# MessageBird: Get Workspace



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-workspace?connectionId=$CONNECTION_ID&organizationId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-workspace?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | The Bird organization ID that owns the workspace. |
| `workspaceId` | string | yes | The Bird workspace ID you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataPolicy": {},
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "status": "string",
      "statusTransitions": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object |  |
| `createdAt` | date | When the workspace was created. |
| `dataPolicy` | object | The data storage policy for a resource. |
| `description` | string | The description for the workspace |
| `id` | string | Workspace ID. |
| `name` | string | The display name for the workspace |
| `organizationId` | string | ID of the organization this workspace is part of. |
| `status` | string | Status of the workspace |
| `statusTransitions` | array<object> |  |
| `updatedAt` | date | When the workspace was last updated. |

## Native endpoint

Through the native MessageBird API, this operation is `GET /organizations/:organizationId/workspaces/:workspaceId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.


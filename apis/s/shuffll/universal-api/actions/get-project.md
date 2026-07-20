# Shuffll: Get Project

Retrieves a project from Shuffll by ID.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/get-project?${params}`, {
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
| `projectId` | string | yes | Shuffll project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "creative": {},
      "id": "string",
      "name": "Ava Chen",
      "scenes": [
        {}
      ],
      "status": "string",
      "statuses": {},
      "updatedAt": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `creative` | object | Creative generation status. |
| `id` | string | Project id. |
| `name` | string | Project name. |
| `scenes` | array<object> | Project scenes. |
| `status` | string | Project status. |
| `statuses` | object | Project status summary. |
| `updatedAt` | string | Last update timestamp. |
| `workspaceId` | string | Workspace id. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/project/:projectId` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.


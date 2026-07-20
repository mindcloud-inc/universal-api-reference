# Mural: Get Workspace

Retrieves a workspace from Mural by ID.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | string | yes | Unique identifier of a workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {},
      "createdOn": 1,
      "description": "string",
      "id": "string",
      "image": "string",
      "locked": true,
      "name": "Ava Chen",
      "sharingSettings": {},
      "suspended": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | object |  |
| `createdOn` | number |  |
| `description` | string |  |
| `id` | string |  |
| `image` | string |  |
| `locked` | boolean |  |
| `name` | string |  |
| `sharingSettings` | object |  |
| `suspended` | boolean |  |

## Native endpoint

Through the native Mural API, this operation is `GET /workspaces/:workspaceId` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.


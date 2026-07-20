# Xano: Get Workspace

Retrieves a workspace from Xano by ID.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-workspace?${params}`, {
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
| `workspace_id` | number | yes | The Xano workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branch": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "swagger": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `swagger` | boolean |  |

## Native endpoint

Through the native Xano API, this operation is `GET /api%3Ameta/workspace/:workspace_id` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.


# Xano: List Workspaces

Finds workspaces in Xano.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/list-workspaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Xano API, this operation is `GET /api%3Ameta/workspace` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.


# Hex: List Collections



```
GET https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hex/latest/actions/list-collections?${params}`, {
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
| `sortBy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {
        "email": "ava@example.com",
        "id": "string"
      },
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "sharing": {
        "users": [
          {}
        ],
        "workspace": {
          "members": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator.email` | string |  |
| `creator.id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `sharing.users` | array<object> |  |
| `sharing.workspace.members` | string |  |

## Native endpoint

Through the native Hex API, this operation is `GET /collections` (base URL `https://app.hex.tech/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.


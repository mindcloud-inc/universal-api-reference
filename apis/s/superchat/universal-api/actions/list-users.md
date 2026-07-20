# Superchat: List Users

Retrieves users from a Superchat workspace.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | string | no | Specify the cursor before which objects should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "inboxes": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "language": "string",
      "last_name": "Chen",
      "role": "string",
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `inboxes` | array<object> |  |
| `inboxes.id` | string |  |
| `inboxes.name` | string |  |
| `inboxes.url` | string |  |
| `language` | string |  |
| `last_name` | string |  |
| `role` | string |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `GET /users` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.


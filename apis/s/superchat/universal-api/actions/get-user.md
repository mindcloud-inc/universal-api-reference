# Superchat: Get User

Retrieves a user from Superchat by ID.

```
GET https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-user?connectionId=$CONNECTION_ID&user_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superchat/latest/actions/get-user?${params}`, {
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
| `user_id` | string | yes | The unique identifier of the user |

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

Through the native Superchat API, this operation is `GET /users/{user_id}` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.


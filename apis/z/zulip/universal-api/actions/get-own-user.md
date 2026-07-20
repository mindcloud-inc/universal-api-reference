# Zulip: Get Own User

Retrieves the requesting user's Zulip account details.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-own-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-own-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-own-user?${params}`, {
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
      "avatar_url": "https://example.com",
      "avatar_version": 1,
      "bot_owner_id": 1,
      "bot_type": 1,
      "date_joined": "string",
      "delivery_email": "ava@example.com",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "is_active": true,
      "is_admin": true,
      "is_bot": true,
      "is_guest": true,
      "is_imported_stub": true,
      "is_owner": true,
      "max_message_id": 1,
      "msg": "string",
      "result": "string",
      "role": 1,
      "timezone": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `avatar_version` | number |  |
| `bot_owner_id` | number |  |
| `bot_type` | number |  |
| `date_joined` | string |  |
| `delivery_email` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `is_active` | boolean |  |
| `is_admin` | boolean |  |
| `is_bot` | boolean |  |
| `is_guest` | boolean |  |
| `is_imported_stub` | boolean |  |
| `is_owner` | boolean |  |
| `max_message_id` | number |  |
| `msg` | string |  |
| `result` | string |  |
| `role` | number |  |
| `timezone` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /users/me` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-own-user.md) for the provider-specific parameters and requirements.


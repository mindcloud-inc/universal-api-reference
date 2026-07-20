# SimpleKPI: List Users

Retrieves user records from a SimpleKPI account.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-users?${params}`, {
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
      "can_admin_settings": true,
      "can_manage_users": true,
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_login_at": "string",
      "last_name": "Chen",
      "last_password_changed_at": "string",
      "password": "string",
      "updated_at": "string",
      "user_status_id": "string",
      "user_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_admin_settings` | boolean |  |
| `can_manage_users` | boolean |  |
| `created_at` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_login_at` | string |  |
| `last_name` | string |  |
| `last_password_changed_at` | string |  |
| `password` | string |  |
| `updated_at` | string |  |
| `user_status_id` | string |  |
| `user_type` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET users` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.


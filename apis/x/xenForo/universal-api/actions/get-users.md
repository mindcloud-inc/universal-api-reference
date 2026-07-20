# XenForo: Get Users

Retrieves a list of users from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-users?${params}`, {
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
      "pagination": {
        "current_page": 1,
        "total": 1
      },
      "users": [
        {
          "email": "ava@example.com",
          "is_admin": true,
          "is_staff": true,
          "last_activity": 1,
          "register_date": 1,
          "user_id": 1,
          "username": "Ava Chen",
          "view_url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.current_page` | number |  |
| `pagination.total` | number |  |
| `users` | array<object> |  |
| `users[].email` | string |  |
| `users[].is_admin` | boolean |  |
| `users[].is_staff` | boolean |  |
| `users[].last_activity` | number |  |
| `users[].register_date` | number |  |
| `users[].user_id` | number |  |
| `users[].username` | string |  |
| `users[].view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /users/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users.md) for the provider-specific parameters and requirements.


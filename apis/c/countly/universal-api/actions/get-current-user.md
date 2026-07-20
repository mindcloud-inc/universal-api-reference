# Countly: Get Current User

Retrieves the current user from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-current-user?${params}`, {
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
      "_id": "string",
      "active_app_id": "string",
      "created_at": 1,
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "global_admin": true,
      "last_login": 1,
      "login_count": 1,
      "session_count": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `active_app_id` | string |  |
| `created_at` | number |  |
| `email` | string |  |
| `full_name` | string |  |
| `global_admin` | boolean |  |
| `last_login` | number |  |
| `login_count` | number |  |
| `session_count` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Countly API, this operation is `GET /o/users/me` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.


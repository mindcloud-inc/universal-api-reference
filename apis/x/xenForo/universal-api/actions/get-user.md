# XenForo: Get User

Retrieves the specified user from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-user?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | ID of the user to retrieve. Example: `123`. |
| `withPosts` | boolean | no | If true, include a page of profile posts with the user response. |

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
      "profile_posts": [
        {}
      ],
      "user": {
        "email": "ava@example.com",
        "is_admin": true,
        "is_staff": true,
        "last_activity": 1,
        "register_date": 1,
        "user_id": 1,
        "username": "Ava Chen",
        "view_url": "https://example.com"
      }
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
| `profile_posts` | array<object> |  |
| `user.email` | string |  |
| `user.is_admin` | boolean |  |
| `user.is_staff` | boolean |  |
| `user.last_activity` | number |  |
| `user.register_date` | number |  |
| `user.user_id` | number |  |
| `user.username` | string |  |
| `user.view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /users/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.


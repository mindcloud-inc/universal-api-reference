# Box: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/box/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/box/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/box/latest/actions/get-current-user?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "enterprise": {},
      "external_app_user_id": "string",
      "hostname": "Ava Chen",
      "id": "string",
      "is_platform_access_only": true,
      "language": "string",
      "login": "string",
      "max_upload_size": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "role": "string",
      "space_amount": 1,
      "space_used": 1,
      "status": "string",
      "timezone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string | URL of the user's avatar image. |
| `created_at` | date | When the user object was created. |
| `enterprise` | object | Representation of the user's enterprise. |
| `external_app_user_id` | string | External identifier for an app user when present. |
| `hostname` | string | Root hostname for Box links for this user. |
| `id` | string | The unique identifier for this user. |
| `is_platform_access_only` | boolean | Whether the user is an App User. |
| `language` | string | The user's language. |
| `login` | string | The primary email address of this user. |
| `max_upload_size` | number | The maximum individual file size in bytes the user can upload. |
| `modified_at` | date | When the user object was last modified. |
| `name` | string | The display name of this user. |
| `role` | string | The user's enterprise role. |
| `space_amount` | number | The user's total available space in bytes. |
| `space_used` | number | The amount of space in use by the user. |
| `status` | string | The user's account status. |
| `timezone` | string | The user's timezone. |
| `type` | string | Always user. |

## Native endpoint

Through the native Box API, this operation is `GET /users/me` (base URL `https://api.box.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.


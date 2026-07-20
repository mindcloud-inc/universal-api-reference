# Codeberg: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user?${params}`, {
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
      "active": true,
      "avatar_url": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "followers_count": 1,
      "following_count": 1,
      "full_name": "Ava Chen",
      "html_url": "https://example.com",
      "id": 1,
      "is_admin": true,
      "language": "string",
      "last_login": "2026-05-07T12:00:00.000Z",
      "login": "string",
      "restricted": true,
      "starred_repos_count": 1,
      "username": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the account is active. |
| `avatar_url` | string | Avatar image URL. |
| `created` | date | Account creation timestamp. |
| `email` | string | Primary email address returned by the API. |
| `followers_count` | number | Follower count. |
| `following_count` | number | Following count. |
| `full_name` | string | Full display name. |
| `html_url` | string | Profile URL. |
| `id` | number | Numeric Codeberg user ID. |
| `is_admin` | boolean | Whether the user is an instance admin. |
| `language` | string | Preferred language. |
| `last_login` | date | Last login timestamp. |
| `login` | string | User login name. |
| `restricted` | boolean | Whether the user account is restricted. |
| `starred_repos_count` | number | Starred repository count. |
| `username` | string | Username. |
| `visibility` | string | Profile visibility. |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.


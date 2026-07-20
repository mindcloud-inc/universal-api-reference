# Codeberg: List Current User Following



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-following
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-following?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-following?${params}`, {
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
| `active` | boolean |  |
| `avatar_url` | string |  |
| `created` | date |  |
| `email` | string |  |
| `followers_count` | number |  |
| `following_count` | number |  |
| `full_name` | string |  |
| `html_url` | string |  |
| `id` | number |  |
| `is_admin` | boolean |  |
| `language` | string |  |
| `last_login` | date |  |
| `login` | string |  |
| `starred_repos_count` | number |  |
| `username` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/following` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-following.md) for the provider-specific parameters and requirements.


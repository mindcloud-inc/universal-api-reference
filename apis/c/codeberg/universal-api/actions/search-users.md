# Codeberg: Search Users



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-users?${params}`, {
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
          "username": "Ava Chen",
          "visibility": "string"
        }
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].active` | boolean |  |
| `data[].avatar_url` | string |  |
| `data[].created` | date |  |
| `data[].email` | string |  |
| `data[].followers_count` | number |  |
| `data[].following_count` | number |  |
| `data[].full_name` | string |  |
| `data[].html_url` | string |  |
| `data[].id` | number |  |
| `data[].is_admin` | boolean |  |
| `data[].language` | string |  |
| `data[].last_login` | date |  |
| `data[].login` | string |  |
| `data[].username` | string |  |
| `data[].visibility` | string |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /users/search` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.


# Codeberg Universal API Examples

These examples use the MindCloud API key and Codeberg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



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

Example response:

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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codeberg/latest/actions/get-current-user).

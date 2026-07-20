# Codeberg: List Current User Organizations



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-organizations?${params}`, {
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
      "description": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "location": "string",
      "name": "Ava Chen",
      "repo_admin_change_team_access": true,
      "username": "Ava Chen",
      "visibility": "string",
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string |  |
| `description` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `location` | string |  |
| `name` | string |  |
| `repo_admin_change_team_access` | boolean |  |
| `username` | string |  |
| `visibility` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/orgs` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-organizations.md) for the provider-specific parameters and requirements.


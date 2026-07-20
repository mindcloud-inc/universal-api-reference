# GitHub Utils: List Authenticated User Organizations

Retrieves organizations for the authenticated GitHub user.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-authenticated-user-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-authenticated-user-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-authenticated-user-organizations?${params}`, {
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
      "events_url": "https://example.com",
      "hooks_url": "https://example.com",
      "id": 1,
      "issues_url": "https://example.com",
      "login": "string",
      "members_url": "https://example.com",
      "node_id": "string",
      "public_members_url": "https://example.com",
      "repos_url": "https://example.com",
      "url": "https://example.com"
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
| `events_url` | string |  |
| `hooks_url` | string |  |
| `id` | number |  |
| `issues_url` | string |  |
| `login` | string |  |
| `members_url` | string |  |
| `node_id` | string |  |
| `public_members_url` | string |  |
| `repos_url` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /user/orgs` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-authenticated-user-organizations.md) for the provider-specific parameters and requirements.


# GitHub Utils: List Authenticated User Repositories

Retrieves repositories for the authenticated GitHub user.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-authenticated-user-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-authenticated-user-repositories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-authenticated-user-repositories?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "default_branch": "string",
      "description": "string",
      "fork": true,
      "forks_count": 1,
      "full_name": "Ava Chen",
      "homepage": "string",
      "html_url": "https://example.com",
      "id": 1,
      "language": "string",
      "name": "Ava Chen",
      "node_id": "string",
      "open_issues_count": 1,
      "owner": {},
      "private": true,
      "pushed_at": "2026-05-07T12:00:00.000Z",
      "stargazers_count": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "watchers_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `default_branch` | string |  |
| `description` | string |  |
| `fork` | boolean |  |
| `forks_count` | number |  |
| `full_name` | string |  |
| `homepage` | string |  |
| `html_url` | string |  |
| `id` | number |  |
| `language` | string |  |
| `name` | string |  |
| `node_id` | string |  |
| `open_issues_count` | number |  |
| `owner` | object |  |
| `private` | boolean |  |
| `pushed_at` | date |  |
| `stargazers_count` | number |  |
| `updated_at` | date |  |
| `url` | string |  |
| `watchers_count` | number |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /user/repos` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-authenticated-user-repositories.md) for the provider-specific parameters and requirements.


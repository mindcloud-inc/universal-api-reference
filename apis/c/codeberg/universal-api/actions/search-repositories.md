# Codeberg: Search Repositories



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-repositories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/search-repositories?${params}`, {
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
          "archived": true,
          "clone_url": "https://example.com",
          "created_at": "2026-05-07T12:00:00.000Z",
          "default_branch": "string",
          "description": "string",
          "empty": true,
          "fork": true,
          "forks_count": 1,
          "full_name": "Ava Chen",
          "html_url": "https://example.com",
          "id": 1,
          "name": "Ava Chen",
          "open_issues_count": 1,
          "owner": {
            "login": "string"
          },
          "private": true,
          "size": 1,
          "ssh_url": "https://example.com",
          "stars_count": 1,
          "updated_at": "2026-05-07T12:00:00.000Z",
          "watchers_count": 1,
          "website": "https://example.com"
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
| `data[].archived` | boolean |  |
| `data[].clone_url` | string |  |
| `data[].created_at` | date |  |
| `data[].default_branch` | string |  |
| `data[].description` | string |  |
| `data[].empty` | boolean |  |
| `data[].fork` | boolean |  |
| `data[].forks_count` | number |  |
| `data[].full_name` | string |  |
| `data[].html_url` | string |  |
| `data[].id` | number |  |
| `data[].name` | string |  |
| `data[].open_issues_count` | number |  |
| `data[].owner.login` | string |  |
| `data[].private` | boolean |  |
| `data[].size` | number |  |
| `data[].ssh_url` | string |  |
| `data[].stars_count` | number |  |
| `data[].updated_at` | date |  |
| `data[].watchers_count` | number |  |
| `data[].website` | string |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /repos/search` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-repositories.md) for the provider-specific parameters and requirements.


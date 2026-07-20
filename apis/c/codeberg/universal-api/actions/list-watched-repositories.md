# Codeberg: List Watched Repositories



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-watched-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-watched-repositories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-watched-repositories?${params}`, {
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `clone_url` | string |  |
| `created_at` | date |  |
| `default_branch` | string |  |
| `description` | string |  |
| `empty` | boolean |  |
| `fork` | boolean |  |
| `forks_count` | number |  |
| `full_name` | string |  |
| `html_url` | string |  |
| `id` | number |  |
| `name` | string |  |
| `open_issues_count` | number |  |
| `owner.login` | string |  |
| `private` | boolean |  |
| `size` | number |  |
| `ssh_url` | string |  |
| `stars_count` | number |  |
| `updated_at` | date |  |
| `watchers_count` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/subscriptions` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-watched-repositories.md) for the provider-specific parameters and requirements.


# GitHub Utils: List Commits

Retrieves commits from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-commits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-commits?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "owner": "string",
  "repo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-commits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "comments_url": "https://example.com",
      "commit": {},
      "committer": {},
      "html_url": "https://example.com",
      "node_id": "string",
      "parents": [
        {}
      ],
      "sha": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `comments_url` | string |  |
| `commit` | object |  |
| `committer` | object |  |
| `html_url` | string |  |
| `node_id` | string |  |
| `parents` | array<object> |  |
| `sha` | string |  |
| `url` | string |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/commits` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-commits.md) for the provider-specific parameters and requirements.


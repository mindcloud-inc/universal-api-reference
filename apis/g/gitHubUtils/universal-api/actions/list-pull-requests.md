# GitHub Utils: List Pull Requests

Retrieves pull requests from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-pull-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-pull-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/list-pull-requests?${params}`, {
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
| `state` | string | no | Pull request state to return. |
| `repo` | string | yes | Repository name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author_association": "string",
      "base": {},
      "body": "string",
      "closed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "diff_url": "https://example.com",
      "draft": true,
      "head": {},
      "html_url": "https://example.com",
      "id": 1,
      "issue_url": "https://example.com",
      "locked": true,
      "merge_commit_sha": "string",
      "merged_at": "2026-05-07T12:00:00.000Z",
      "node_id": "string",
      "number": 1,
      "patch_url": "https://example.com",
      "state": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author_association` | string |  |
| `base` | object |  |
| `body` | string |  |
| `closed_at` | date |  |
| `created_at` | date |  |
| `diff_url` | string |  |
| `draft` | boolean |  |
| `head` | object |  |
| `html_url` | string |  |
| `id` | number |  |
| `issue_url` | string |  |
| `locked` | boolean |  |
| `merge_commit_sha` | string |  |
| `merged_at` | date |  |
| `node_id` | string |  |
| `number` | number |  |
| `patch_url` | string |  |
| `state` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/pulls` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pull-requests.md) for the provider-specific parameters and requirements.


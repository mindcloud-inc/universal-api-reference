# GitHub Utils: Get Pull Request

Retrieves a pull request from a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-pull-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-pull-request?connectionId=$CONNECTION_ID&owner=string&repo=string&pull_number=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "pull_number": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-pull-request?${params}`, {
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
| `pull_number` | number | yes | Pull request number in the repository. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additions": 1,
      "author_association": "string",
      "base": {},
      "body": "string",
      "changed_files": 1,
      "closed_at": "2026-05-07T12:00:00.000Z",
      "comments": 1,
      "commits": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "deletions": 1,
      "diff_url": "https://example.com",
      "draft": true,
      "head": {},
      "html_url": "https://example.com",
      "id": 1,
      "issue_url": "https://example.com",
      "locked": true,
      "merge_commit_sha": "string",
      "mergeable": true,
      "merged": true,
      "merged_at": "2026-05-07T12:00:00.000Z",
      "node_id": "string",
      "number": 1,
      "patch_url": "https://example.com",
      "review_comments": 1,
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
| `additions` | number |  |
| `author_association` | string |  |
| `base` | object |  |
| `body` | string |  |
| `changed_files` | number |  |
| `closed_at` | date |  |
| `comments` | number |  |
| `commits` | number |  |
| `created_at` | date |  |
| `deletions` | number |  |
| `diff_url` | string |  |
| `draft` | boolean |  |
| `head` | object |  |
| `html_url` | string |  |
| `id` | number |  |
| `issue_url` | string |  |
| `locked` | boolean |  |
| `merge_commit_sha` | string |  |
| `mergeable` | boolean |  |
| `merged` | boolean |  |
| `merged_at` | date |  |
| `node_id` | string |  |
| `number` | number |  |
| `patch_url` | string |  |
| `review_comments` | number |  |
| `state` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /repos/:owner/:repo/pulls/:pull_number` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pull-request.md) for the provider-specific parameters and requirements.


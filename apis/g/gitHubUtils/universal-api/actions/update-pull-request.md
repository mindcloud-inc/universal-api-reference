# GitHub Utils: Update Pull Request

Updates an existing pull request on GitHub.

```
PUT https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/update-pull-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/update-pull-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "pull_number": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/update-pull-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "pull_number": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | New pull request body. |
| `owner` | string | yes | Repository owner or organization login. |
| `state` | string | no | Pull request state, such as open or closed. |
| `title` | string | no | New pull request title. |
| `repo` | string | yes | Repository name. |
| `pull_number` | number | yes | Pull request number in the repository. |

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

Through the native GitHub Utils API, this operation is `PATCH /repos/:owner/:repo/pulls/:pull_number` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pull-request.md) for the provider-specific parameters and requirements.


# GitHub: Merge Pull Request

Merges a pull request into the base branch in GitHub.

```
PUT https://connect.mindcloud.co/v1/universal/github/latest/actions/merge-pull-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/github/latest/actions/merge-pull-request" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/merge-pull-request', {
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
| `owner` | string | yes | Repository owner or organization login. |
| `repo` | string | yes | Repository name. |
| `pull_number` | number | yes | Pull request number. |
| `merge_method` | list<string> | no | The merge method to use. One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commit_title` | string | no | Title for the automatic commit message. |
| `commit_message` | string | no | Extra detail to append to the automatic commit message. |
| `sha` | string | no | SHA that the pull request head must match to allow the merge. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `PUT /repos/:owner/:repo/pulls/:pull_number/merge` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-pull-request.md) for the provider-specific parameters and requirements.


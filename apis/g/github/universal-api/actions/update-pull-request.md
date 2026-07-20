# GitHub: Update Pull Request

Updates a pull request in a GitHub repository.

```
PUT https://connect.mindcloud.co/v1/universal/github/latest/actions/update-pull-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/github/latest/actions/update-pull-request" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/update-pull-request', {
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
| `title` | string | no | The title of the pull request. |
| `body` | string | no | The contents of the pull request. |
| `state` | list<string> | no | The state of the pull request. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base` | string | no | The branch you want the changes pulled into. |
| `maintainer_can_modify` | boolean | no | Whether maintainers can modify the pull request branch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `PATCH /repos/:owner/:repo/pulls/:pull_number` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pull-request.md) for the provider-specific parameters and requirements.


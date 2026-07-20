# GitHub: Create Pull Request

Creates a pull request in a GitHub repository.

```
POST https://connect.mindcloud.co/v1/universal/github/latest/actions/create-pull-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/github/latest/actions/create-pull-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "head": "string",
  "base": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/create-pull-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "head": "string",
    "base": "string"
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
| `title` | string | no | The title of the new pull request. |
| `head` | string | yes | The branch where the changes are implemented. |
| `base` | string | yes | The branch you want the changes pulled into. |
| `body` | string | no | The contents of the pull request. |
| `draft` | boolean | no | Whether the pull request is a draft. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `head_repo` | string | no | The repository where the changes in the pull request were made when required. |
| `maintainer_can_modify` | boolean | no | Whether maintainers can modify the pull request branch. |
| `issue` | number | no | An existing issue number to convert into a pull request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `POST /repos/:owner/:repo/pulls` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pull-request.md) for the provider-specific parameters and requirements.


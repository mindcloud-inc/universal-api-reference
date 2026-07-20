# GitHub: Create or Update File Content

Creates or updates a file in a GitHub repository.

```
PUT https://connect.mindcloud.co/v1/universal/github/latest/actions/create-or-update-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/github/latest/actions/create-or-update-file-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "path": "string",
  "message": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/create-or-update-file-content', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "path": "string",
    "message": "string",
    "content": "string"
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
| `path` | string | yes | Path to the file within the repository. |
| `message` | string | yes | The commit message. |
| `content` | string | yes | The new file content, using Base64 encoding. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sha` | string | no | The blob SHA of the file being replaced when updating an existing file. |
| `branch` | string | no | The branch name. Defaults to the repository default branch. |
| `committer` | object | no | Committer information. Defaults to the authenticated user. |
| `committer.name` | string | no | The name of the committer. |
| `committer.email` | string | no | The email of the committer. |
| `committer.date` | date | no | The commit date for the committer. |
| `author` | object | no | Author information. Defaults to the committer or authenticated user. |
| `author.name` | string | no | The name of the author. |
| `author.email` | string | no | The email of the author. |
| `author.date` | date | no | The commit date for the author. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `PUT /repos/:owner/:repo/contents/:path` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-file-content.md) for the provider-specific parameters and requirements.


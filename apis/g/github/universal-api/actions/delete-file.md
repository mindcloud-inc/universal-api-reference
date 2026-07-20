# GitHub: Delete File

Deletes a file from a GitHub repository.

```
DELETE https://connect.mindcloud.co/v1/universal/github/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/github/latest/actions/delete-file?connectionId=$CONNECTION_ID&owner=string&repo=string&path=string&message=string&sha=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "owner": "string",
  "repo": "string",
  "path": "string",
  "message": "string",
  "sha": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/delete-file?${params}`, {
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
| `path` | string | yes | Path to the file within the repository. |
| `message` | string | yes | The commit message. |
| `sha` | string | yes | The blob SHA of the file being deleted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branch` | string | no | The branch name. Defaults to the repository default branch. |
| `committer` | object | no | Committer information. |
| `committer.name` | string | no | The name of the committer. |
| `committer.email` | string | no | The email of the committer. |
| `author` | object | no | Author information. |
| `author.name` | string | no | The name of the author. |
| `author.email` | string | no | The email of the author. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `DELETE /repos/:owner/:repo/contents/:path` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.


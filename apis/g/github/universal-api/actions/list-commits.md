# GitHub: List Commits

Lists commits in a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-commits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-commits?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-commits?${params}`, {
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
| `owner` | string | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | string | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `sha` | string | no | SHA or branch to start listing commits from. |
| `path` | string | no | Only commits containing this file path will be returned. |
| `author` | string | no | GitHub username or email address to use to filter by commit author. |
| `committer` | string | no | GitHub username or email address to use to filter by commit committer. |
| `since` | string | no | Only show results after this ISO 8601 timestamp. |
| `until` | string | no | Only show results before this ISO 8601 timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/commits` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-commits.md) for the provider-specific parameters and requirements.


# GitHub: List Pull Requests

Lists pull requests in a GitHub repository.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/list-pull-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/list-pull-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&owner=string&repo=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/list-pull-requests?${params}`, {
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
| `state` | string | no | Pull request state to return. One of: `0`, `1`, `2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `GET /repos/:owner/:repo/pulls` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pull-requests.md) for the provider-specific parameters and requirements.


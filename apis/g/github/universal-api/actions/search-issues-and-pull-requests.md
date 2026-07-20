# GitHub: Search Issues and Pull Requests

Finds GitHub issues and pull requests by search query.

```
GET https://connect.mindcloud.co/v1/universal/github/latest/actions/search-issues-and-pull-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/search-issues-and-pull-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/github/latest/actions/search-issues-and-pull-requests?${params}`, {
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
| `q` | string | no | Optional free-text GitHub search query. Structured filters are also appended into the final q search string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advanced_search` | string | no | Set true to opt into advanced search syntax when needed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GitHub API returns.

## Native endpoint

Through the native GitHub API, this operation is `GET /search/issues` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-issues-and-pull-requests.md) for the provider-specific parameters and requirements.


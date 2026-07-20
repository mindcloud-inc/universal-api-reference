# GitHub Utils: Search Issues and Pull Requests

Finds issues and pull requests on GitHub by query.

```
GET https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/search-issues-and-pull-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub Utils `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/search-issues-and-pull-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/search-issues-and-pull-requests?${params}`, {
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
| `q` | string | yes | Search query using GitHub issue and pull request search syntax. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "incomplete_results": true,
      "items": [
        {}
      ],
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `incomplete_results` | boolean |  |
| `items` | array<object> |  |
| `total_count` | number |  |

## Native endpoint

Through the native GitHub Utils API, this operation is `GET /search/issues` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-issues-and-pull-requests.md) for the provider-specific parameters and requirements.


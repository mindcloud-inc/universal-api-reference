# NewsData.io: List Latest News



```
GET https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-latest-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsData.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-latest-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-latest-news?${params}`, {
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
| `category` | string | no | Category filter for latest news results. |
| `country` | string | no | Country code filter for latest news results. |
| `domainUrl` | string | no | Filter latest news by one or more source domain URLs. |
| `language` | string | no | Language code filter for latest news results. |
| `q` | string | no | Keyword or phrase to search for in latest news results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": "string",
      "results": [
        {}
      ],
      "status": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | string | Pagination token for the next page when more results are available. |
| `results` | array<object> | Returned news articles. |
| `status` | string | Request status. |
| `totalResults` | number | Total number of matching articles. |

## Native endpoint

Through the native NewsData.io API, this operation is `GET /latest` (base URL `https://newsdata.io/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-latest-news.md) for the provider-specific parameters and requirements.


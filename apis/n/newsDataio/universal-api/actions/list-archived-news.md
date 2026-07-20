# NewsData.io: List Archived News



```
GET https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-archived-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsData.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-archived-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-archived-news?${params}`, {
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
| `category` | string | no | Category filter for archived news results. |
| `country` | string | no | Country code filter for archived news results. |
| `fromDate` | string | no | Start date for archived news retrieval. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. Example: `2026-04-20`. |
| `language` | string | no | Language code filter for archived news results. |
| `q` | string | no | Keyword or phrase to search for in archived news results. |
| `toDate` | string | no | End date for archived news retrieval. Use `YYYY-MM-DD` or `YYYY-MM-DD HH:MM:SS`. Example: `2026-04-21`. |

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
| `results` | array<object> | Returned archived news articles. |
| `status` | string | Request status. |
| `totalResults` | number | Total number of matching archived articles. |

## Native endpoint

Through the native NewsData.io API, this operation is `GET /archive` (base URL `https://newsdata.io/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-archived-news.md) for the provider-specific parameters and requirements.


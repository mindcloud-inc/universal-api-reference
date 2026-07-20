# NewsData.io: List Crypto News



```
GET https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-crypto-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsData.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-crypto-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-crypto-news?${params}`, {
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
| `country` | string | no | Country code filter for crypto news results. |
| `language` | string | no | Language code filter for crypto news results. |
| `q` | string | no | Keyword or phrase to search for in crypto news results. |

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
| `results` | array<object> | Returned crypto news articles. |
| `status` | string | Request status. |
| `totalResults` | number | Total number of matching articles. |

## Native endpoint

Through the native NewsData.io API, this operation is `GET /crypto` (base URL `https://newsdata.io/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crypto-news.md) for the provider-specific parameters and requirements.


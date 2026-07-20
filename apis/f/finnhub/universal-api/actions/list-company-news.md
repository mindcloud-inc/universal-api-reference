# Finnhub: List Company News

Retrieves company news from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-company-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-company-news?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL&from=2026-04-07&to=2026-04-14" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL",
  "from": "2026-04-07",
  "to": "2026-04-14"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-company-news?${params}`, {
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
| `symbol` | string | yes | Company symbol for news, such as AAPL. Example: `e.g. AAPL`. |
| `from` | string | yes | Start date in YYYY-MM-DD format. Example: `2026-04-07`. |
| `to` | string | yes | End date in YYYY-MM-DD format. Example: `2026-04-14`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "datetime": 1,
      "headline": "string",
      "id": 1,
      "image": "string",
      "related": "string",
      "source": "string",
      "summary": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `datetime` | number |  |
| `headline` | string |  |
| `id` | number |  |
| `image` | string |  |
| `related` | string |  |
| `source` | string |  |
| `summary` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /company-news` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-news.md) for the provider-specific parameters and requirements.


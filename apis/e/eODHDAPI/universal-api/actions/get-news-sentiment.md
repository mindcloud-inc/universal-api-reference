# EODHD: Get News Sentiment

Retrieves news sentiment for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-news-sentiment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-news-sentiment?connectionId=$CONNECTION_ID&s=aapl.us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "s": "aapl.us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-news-sentiment?${params}`, {
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
| `s` | string | yes | Ticker symbol, for example aapl.us. Example: `aapl.us`. |
| `from` | date | no | Start date in YYYY-MM-DD format. Example: `2025-01-01`. |
| `to` | date | no | End date in YYYY-MM-DD format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "normalized": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Mention count. |
| `date` | date | Sentiment date. |
| `normalized` | number | Normalized sentiment score. |

## Native endpoint

Through the native EODHD API, this operation is `GET /sentiments` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-news-sentiment.md) for the provider-specific parameters and requirements.


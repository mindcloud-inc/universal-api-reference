# EODHD: List Earnings Trends

Retrieves earnings trends for symbols from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-earnings-trends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-earnings-trends?connectionId=$CONNECTION_ID&symbols=AAPL.US%2CMSFT.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbols": "AAPL.US,MSFT.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-earnings-trends?${params}`, {
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
| `symbols` | string | yes | Comma-separated EODHD tickers for earnings trend lookup. Example: `AAPL.US,MSFT.US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "earningsEstimateAvg": 1,
      "earningsEstimateHigh": 1,
      "earningsEstimateLow": 1,
      "growth": 1,
      "period": "string",
      "revenueEstimateAvg": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Ticker code. |
| `date` | date | Trend date. |
| `earningsEstimateAvg` | number | Average earnings estimate. |
| `earningsEstimateHigh` | number | High earnings estimate. |
| `earningsEstimateLow` | number | Low earnings estimate. |
| `growth` | number | Growth value. |
| `period` | string | Earnings period. |
| `revenueEstimateAvg` | number | Average revenue estimate. |

## Native endpoint

Through the native EODHD API, this operation is `GET /calendar/trends` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-earnings-trends.md) for the provider-specific parameters and requirements.


# EODHD: List EOD Historical Prices

Retrieves end-of-day historical prices for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-eod-historical-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-eod-historical-prices?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-eod-historical-prices?${params}`, {
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
| `symbol` | string | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. Example: `AAPL.US`. |
| `from` | date | no | Start date in `YYYY-MM-DD` format. Example: `2025-01-01`. |
| `to` | date | no | End date in `YYYY-MM-DD` format. Example: `2025-12-31`. |
| `period` | string | no | Historical price period, such as `d`, `w`, or `m`. Example: `d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adjusted_close": 1,
      "close": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "high": 1,
      "low": 1,
      "open": 1,
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjusted_close` | number | Adjusted close price. |
| `close` | number | Close price. |
| `date` | date | Price date. |
| `high` | number | High price. |
| `low` | number | Low price. |
| `open` | number | Open price. |
| `volume` | number | Trading volume. |

## Native endpoint

Through the native EODHD API, this operation is `GET /eod/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-eod-historical-prices.md) for the provider-specific parameters and requirements.


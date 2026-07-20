# EODHD: List Intraday Prices

Retrieves intraday prices for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-intraday-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-intraday-prices?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-intraday-prices?${params}`, {
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
| `interval` | string | no | Intraday interval, such as `1m`, `5m`, or `1h`. Example: `5m`. |
| `from` | date | no | Start date/time accepted by EODHD intraday history. Example: `2025-01-01`. |
| `to` | date | no | End date/time accepted by EODHD intraday history. Example: `2025-01-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "close": 1,
      "datetime": "string",
      "gmtoffset": 1,
      "high": 1,
      "low": 1,
      "open": 1,
      "timestamp": 1,
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `close` | number | Close price. |
| `datetime` | string | Bar datetime. |
| `gmtoffset` | number | GMT offset in seconds. |
| `high` | number | High price. |
| `low` | number | Low price. |
| `open` | number | Open price. |
| `timestamp` | number | Unix timestamp. |
| `volume` | number | Volume. |

## Native endpoint

Through the native EODHD API, this operation is `GET /intraday/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-intraday-prices.md) for the provider-specific parameters and requirements.


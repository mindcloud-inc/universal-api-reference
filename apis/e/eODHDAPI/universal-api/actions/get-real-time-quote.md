# EODHD: Get Real-Time Quote

Retrieves a real-time quote for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-real-time-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-real-time-quote?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-real-time-quote?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "change": 1,
      "change_p": 1,
      "close": 1,
      "code": "string",
      "gmtoffset": 1,
      "high": 1,
      "low": 1,
      "open": 1,
      "previousClose": 1,
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
| `change` | number | Absolute price change. |
| `change_p` | number | Percentage price change. |
| `close` | number | Latest close or price. |
| `code` | string | Instrument code. |
| `gmtoffset` | number | GMT offset in seconds. |
| `high` | number | High price. |
| `low` | number | Low price. |
| `open` | number | Open price. |
| `previousClose` | number | Previous close. |
| `timestamp` | number | Unix timestamp. |
| `volume` | number | Volume. |

## Native endpoint

Through the native EODHD API, this operation is `GET /real-time/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-real-time-quote.md) for the provider-specific parameters and requirements.


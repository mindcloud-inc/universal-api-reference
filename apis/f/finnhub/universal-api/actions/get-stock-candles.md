# Finnhub: Get Stock Candles

Retrieves stock candles from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-candles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-candles?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL&resolution=e.g.%20D&from=e.g.%201735689600&to=e.g.%201738281600" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL",
  "resolution": "e.g. D",
  "from": "e.g. 1735689600",
  "to": "e.g. 1738281600"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-candles?${params}`, {
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
| `symbol` | string | yes | Company symbol for candles, such as AAPL. Example: `e.g. AAPL`. |
| `resolution` | string | yes | Supported candle resolution, such as 1, 5, 15, 30, 60, D, W, or M. Example: `e.g. D`. |
| `from` | number | yes | Start time as a UNIX timestamp in seconds. Example: `e.g. 1735689600`. |
| `to` | number | yes | End time as a UNIX timestamp in seconds. Example: `e.g. 1738281600`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "c": [
        1
      ],
      "h": [
        1
      ],
      "l": [
        1
      ],
      "o": [
        1
      ],
      "s": "string",
      "t": [
        1
      ],
      "v": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `c` | array<number> | Close prices. |
| `h` | array<number> | High prices. |
| `l` | array<number> | Low prices. |
| `o` | array<number> | Open prices. |
| `s` | string | Status. |
| `t` | array<number> | Unix timestamps. |
| `v` | array<number> | Volume values. |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/candle` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-candles.md) for the provider-specific parameters and requirements.


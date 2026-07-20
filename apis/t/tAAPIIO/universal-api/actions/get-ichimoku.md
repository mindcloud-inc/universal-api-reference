# TAAPI.IO: Get Ichimoku Cloud

Retrieves Ichimoku Cloud indicator data from TAAPI.IO.

```
GET https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-ichimoku
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAAPI.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-ichimoku?connectionId=$CONNECTION_ID&exchange=binance&symbol=BTC%2FUSDT&interval=1h" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "binance",
  "symbol": "BTC/USDT",
  "interval": "1h"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-ichimoku?${params}`, {
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
| `exchange` | string | yes | Example: `binance`. |
| `symbol` | string | yes | Example: `BTC/USDT`. |
| `interval` | string | yes | Example: `1h`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": 1,
      "conversion": 1,
      "currentSpanA": 1,
      "currentSpanB": 1,
      "laggingSpanA": 1,
      "laggingSpanB": 1,
      "spanA": 1,
      "spanB": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | number |  |
| `conversion` | number |  |
| `currentSpanA` | number |  |
| `currentSpanB` | number |  |
| `laggingSpanA` | number |  |
| `laggingSpanB` | number |  |
| `spanA` | number |  |
| `spanB` | number |  |

## Native endpoint

Through the native TAAPI.IO API, this operation is `GET /ichimoku` (base URL `https://api.taapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ichimoku.md) for the provider-specific parameters and requirements.


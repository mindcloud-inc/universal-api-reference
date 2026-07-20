# TAAPI.IO: Get RSI

Retrieves RSI indicator data from TAAPI.IO.

```
GET https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-rsi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAAPI.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-rsi?connectionId=$CONNECTION_ID&exchange=binance&symbol=BTC%2FUSDT&interval=1h" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "binance",
  "symbol": "BTC/USDT",
  "interval": "1h"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-rsi?${params}`, {
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
| `exchange` | string | yes | Exchange to source the indicator data from, such as binance. Example: `binance`. |
| `symbol` | string | yes | Trading pair symbol such as BTC/USDT. Example: `BTC/USDT`. |
| `interval` | string | yes | Timeframe such as 1h or 1d. Example: `1h`. |
| `period` | number | no |  |
| `backtrack` | number | no |  |
| `chart` | string | no |  |
| `addResultTimestamp` | boolean | no |  |
| `fromTimestamp` | string | no |  |
| `toTimestamp` | string | no |  |
| `results` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number |  |

## Native endpoint

Through the native TAAPI.IO API, this operation is `GET /rsi` (base URL `https://api.taapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rsi.md) for the provider-specific parameters and requirements.


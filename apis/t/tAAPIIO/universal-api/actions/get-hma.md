# TAAPI.IO: Get Hull Moving Average

Retrieves Hull Moving Average indicator data from TAAPI.IO.

```
GET https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-hma
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAAPI.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-hma?connectionId=$CONNECTION_ID&exchange=binance&symbol=BTC%2FUSDT&interval=1h&period=50&period=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "binance",
  "symbol": "BTC/USDT",
  "interval": "1h",
  "period": "50",
  "period": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-hma?${params}`, {
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
| `period` | number | yes | Example: `50`. |
| `period` | number | yes | Example: `50`. |

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

Through the native TAAPI.IO API, this operation is `GET /hma` (base URL `https://api.taapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hma.md) for the provider-specific parameters and requirements.


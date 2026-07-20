# TAAPI.IO: Get Awesome Oscillator

Retrieves Awesome Oscillator indicator data from TAAPI.IO.

```
GET https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-awesome-oscillator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAAPI.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-awesome-oscillator?connectionId=$CONNECTION_ID&exchange=string&symbol=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "string",
  "symbol": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-awesome-oscillator?${params}`, {
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
| `exchange` | string | yes | Exchange to source the indicator data from, such as binance. |
| `symbol` | string | yes | Trading pair symbol such as BTC/USDT. |
| `interval` | string | yes | Timeframe such as 1h or 1d. |

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

Through the native TAAPI.IO API, this operation is `GET /ao` (base URL `https://api.taapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-awesome-oscillator.md) for the provider-specific parameters and requirements.


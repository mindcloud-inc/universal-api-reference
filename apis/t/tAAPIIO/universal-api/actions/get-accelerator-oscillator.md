# TAAPI.IO: Get Accelerator Oscillator

Retrieves Accelerator Oscillator indicator data from TAAPI.IO.

```
GET https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-accelerator-oscillator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAAPI.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-accelerator-oscillator?connectionId=$CONNECTION_ID&exchange=string&symbol=string&interval=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "string",
  "symbol": "string",
  "interval": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-accelerator-oscillator?${params}`, {
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
| `lengthSlow` | number | no | Optional slow length for the oscillator calculation. |
| `lengthFast` | number | no | Optional fast length for the oscillator calculation. |

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

Through the native TAAPI.IO API, this operation is `GET /accosc` (base URL `https://api.taapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-accelerator-oscillator.md) for the provider-specific parameters and requirements.


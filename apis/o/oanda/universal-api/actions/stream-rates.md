# Oanda: Stream Rates

Streams live exchange rates from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/stream-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/stream-rates?connectionId=$CONNECTION_ID&base=EUR&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base": "EUR",
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/stream-rates?${params}`, {
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
| `base` | string | yes | Base currency or comma-separated list. Default: `EUR`. |
| `data_set` | string | no | Dataset code. |
| `ext` | string | yes | Response format. Default: `json`. |
| `quote` | string | no | Quote currency or comma-separated list. |
| `tenor` | string | no | Forward tenor or comma-separated list of tenors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "quotes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Stream metadata when available. |
| `quotes` | array<object> | Streaming quote payload. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/rates/stream.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-rates.md) for the provider-specific parameters and requirements.


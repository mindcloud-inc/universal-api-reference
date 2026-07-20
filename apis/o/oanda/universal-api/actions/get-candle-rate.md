# Oanda: Get Candle Rate

Retrieves one daily candle rate from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-candle-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-candle-rate?connectionId=$CONNECTION_ID&base=EUR&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base": "EUR",
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-candle-rate?${params}`, {
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
| `date_time` | string | no | ISO 8601 timestamp on a 15-minute boundary. |
| `decimal_places` | string | no | Decimal precision or all. |
| `ext` | string | yes | Response format. Default: `json`. |
| `fields` | string | no | Comma-separated response fields. |
| `interbank` | string | no | Interbank pricing multiplier. |
| `quote` | string | no | Quote currency or comma-separated list. |
| `source_date` | string | no | Historical source date. |

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
| `meta` | object | Request metadata and effective parameters. |
| `quotes` | array<object> | Candle quote payload. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/rates/candle.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candle-rate.md) for the provider-specific parameters and requirements.


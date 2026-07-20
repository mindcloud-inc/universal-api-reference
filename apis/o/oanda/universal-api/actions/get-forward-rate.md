# Oanda: Get Forward Rate

Retrieves forward rates from Oanda by tenor.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-forward-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-forward-rate?connectionId=$CONNECTION_ID&base=EUR&ext=json&quote=USD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base": "EUR",
  "ext": "json",
  "quote": "USD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-forward-rate?${params}`, {
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
| `base` | string | yes | Base currency code. Default: `EUR`. |
| `ext` | string | yes | Response format. Default: `json`. |
| `quote` | string | yes | Quote currency code. Default: `USD`. |
| `source_date` | string | no | Historical source date. |
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
| `meta` | object | Request metadata and effective parameters. |
| `quotes` | array<object> | Forward quotes for requested tenors. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v2/rates/forward.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forward-rate.md) for the provider-specific parameters and requirements.


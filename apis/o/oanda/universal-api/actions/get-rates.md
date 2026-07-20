# Oanda: Get Rates

Retrieves exchange rates from Oanda for one base currency.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-rates?connectionId=$CONNECTION_ID&base=EUR&ext=json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "base": "EUR",
  "ext": "json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-rates?${params}`, {
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
| `data_set` | string | no | Dataset code. |
| `date` | string | no | Historical date in YYYY-MM-DD. |
| `decimal_places` | string | no | Decimal precision or all. |
| `end` | string | no | End date in YYYY-MM-DD. |
| `ext` | string | yes | Response format. Default: `json`. |
| `fields` | string | no | Comma-separated response fields. |
| `quote` | string | no | Quote currency or comma-separated list of quote currencies. |
| `start` | string | no | Start date in YYYY-MM-DD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_currency": "string",
      "meta": {},
      "quotes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_currency` | string | Base currency code. |
| `meta` | object | Request metadata and effective parameters. |
| `quotes` | object | Quote map keyed by quote currency. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v1/rates/:base.:ext` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rates.md) for the provider-specific parameters and requirements.


# GoCardless: Get Payment

Retrieves a single payment from GoCardless.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-payment?connectionId=$CONNECTION_ID&identity=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identity": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/get-payment?${params}`, {
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
| `identity` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payments": {
        "amount": 1,
        "amountRefunded": 1,
        "chargeDate": "string",
        "createdAt": "string",
        "currency": "string",
        "description": {},
        "fx": {
          "estimatedExchangeRate": {},
          "exchangeRate": {},
          "fxAmount": {},
          "fxCurrency": {}
        },
        "id": "string",
        "links": {
          "creditor": "https://example.com",
          "mandate": "https://example.com"
        },
        "reference": {},
        "retryIfPossible": true,
        "scheme": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payments.amount` | number |  |
| `payments.amountRefunded` | number |  |
| `payments.chargeDate` | string |  |
| `payments.createdAt` | string |  |
| `payments.currency` | string |  |
| `payments.description` | object |  |
| `payments.fx.estimatedExchangeRate` | object |  |
| `payments.fx.exchangeRate` | object |  |
| `payments.fx.fxAmount` | object |  |
| `payments.fx.fxCurrency` | object |  |
| `payments.id` | string |  |
| `payments.links.creditor` | string |  |
| `payments.links.mandate` | string |  |
| `payments.reference` | object |  |
| `payments.retryIfPossible` | boolean |  |
| `payments.scheme` | string |  |
| `payments.status` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /payments/:identity` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment.md) for the provider-specific parameters and requirements.


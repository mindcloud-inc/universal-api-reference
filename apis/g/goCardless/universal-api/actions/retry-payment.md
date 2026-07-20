# GoCardless: Retry Payment

Retries an existing payment in GoCardless.

```
PUT https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/retry-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/retry-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/retry-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identity` | string | yes |  |
| `data.charge_date` | date | no |  |
| `data.metadata` | object | no |  |

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

Through the native GoCardless API, this operation is `POST /payments/:identity/actions/retry` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retry-payment.md) for the provider-specific parameters and requirements.


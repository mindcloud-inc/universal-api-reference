# GoCardless: Create Payment

Creates a new payment in GoCardless.

```
POST https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payments.amount": 1,
  "payments.currency": "string",
  "payments.links.mandate": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payments.amount": 1,
    "payments.currency": "string",
    "payments.links.mandate": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payments.amount` | number | yes |  |
| `payments.currency` | string | yes |  |
| `payments.links.mandate` | string | yes |  |
| `payments.charge_date` | date | no |  |
| `payments.description` | string | no |  |
| `payments.app_fee` | number | no |  |
| `payments.faster_ach` | boolean | no |  |
| `payments.retry_if_possible` | boolean | no |  |
| `payments.psu_interaction_type` | string | no |  |
| `payments.metadata` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payments.reference` | string | no |  |

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
          "estimatedExchangeRate": "string",
          "exchangeRate": {},
          "fxAmount": {},
          "fxCurrency": "string"
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
| `payments.fx.estimatedExchangeRate` | string |  |
| `payments.fx.exchangeRate` | object |  |
| `payments.fx.fxAmount` | object |  |
| `payments.fx.fxCurrency` | string |  |
| `payments.id` | string |  |
| `payments.links.creditor` | string |  |
| `payments.links.mandate` | string |  |
| `payments.reference` | object |  |
| `payments.retryIfPossible` | boolean |  |
| `payments.scheme` | string |  |
| `payments.status` | string |  |

## Native endpoint

Through the native GoCardless API, this operation is `POST /payments` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.


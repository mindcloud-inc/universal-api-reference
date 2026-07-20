# Quaderno: Record Invoice Payment

Records a payment for an invoice in Quaderno.

```
POST https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/record-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/record-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/record-invoice-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Payment amount. |
| `date` | date | no | Payment date. |
| `id` | string | yes | The ID of the invoice to record payment for. |
| `paymentMethod` | string | no | Payment method. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountCents": 1,
      "date": "string",
      "id": 1,
      "paymentMethod": "string",
      "processor": {},
      "processorId": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountCents` | number |  |
| `date` | string |  |
| `id` | number |  |
| `paymentMethod` | string |  |
| `processor` | object |  |
| `processorId` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Quaderno API, this operation is `POST /invoices/:id/payments` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-invoice-payment.md) for the provider-specific parameters and requirements.


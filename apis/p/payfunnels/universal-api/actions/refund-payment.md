# Payfunnels: Refund Payment

Updates a payment by refunding it in Payfunnels.

```
PUT https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/refund-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/refund-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "id": "string",
  "reason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/refund-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "id": "string",
    "reason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | The amount to refund in the smallest currency unit. |
| `id` | string | yes | The ID of the payment to refund. |
| `reason` | string | yes | Reason for the refund: duplicate, fraudulent, or requested_by_customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {},
      "cardLast4": "string",
      "coupon": {},
      "createdAt": "string",
      "currencyCode": "string",
      "customer": {},
      "description": "string",
      "id": "string",
      "metadata": {},
      "processingFeeAmount": 1,
      "products": [
        {}
      ],
      "quantity": 1,
      "refundAmount": 1,
      "setupFeeAmount": 1,
      "shippingAddress": {},
      "status": "string",
      "taxAmount": 1,
      "title": "string",
      "totalAmountPaid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `cardLast4` | string |  |
| `coupon` | object |  |
| `createdAt` | string |  |
| `currencyCode` | string |  |
| `customer` | object |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `processingFeeAmount` | number |  |
| `products` | array<object> |  |
| `quantity` | number |  |
| `refundAmount` | number |  |
| `setupFeeAmount` | number |  |
| `shippingAddress` | object |  |
| `status` | string |  |
| `taxAmount` | number |  |
| `title` | string |  |
| `totalAmountPaid` | number |  |

## Native endpoint

Through the native Payfunnels API, this operation is `POST /v1/payments/refund` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-payment.md) for the provider-specific parameters and requirements.


# Razorpay: Create Payment Refund

Creates a refund for a payment in Razorpay.

```
POST https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-payment-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-payment-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/create-payment-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the payment. |
| `amount` | number | no |  |
| `speed` | string | no |  |
| `notes` | object | no |  |
| `receipt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acquirerData": {},
      "amount": 1,
      "batchId": "string",
      "createdAt": 1,
      "currency": "string",
      "entity": "string",
      "id": "string",
      "notes": {},
      "paymentId": "string",
      "receipt": "string",
      "speedProcessed": "string",
      "speedRequested": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acquirerData` | object |  |
| `amount` | number |  |
| `batchId` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `entity` | string |  |
| `id` | string |  |
| `notes` | object |  |
| `paymentId` | string |  |
| `receipt` | string |  |
| `speedProcessed` | string |  |
| `speedRequested` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `POST /v1/payments/:id/refund` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-refund.md) for the provider-specific parameters and requirements.


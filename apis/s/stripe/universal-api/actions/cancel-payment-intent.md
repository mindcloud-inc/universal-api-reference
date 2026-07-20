# Stripe: Cancel Payment Intent

Cancels an existing payment intent in Stripe.

```
PUT https://connect.mindcloud.co/v1/universal/stripe/latest/actions/cancel-payment-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/cancel-payment-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "intent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/cancel-payment-intent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "intent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `intent` | string | yes | PaymentIntent ID to cancel. |
| `cancellationReason` | list<string> | no | Reason for cancellation. One of: `abandoned`, `duplicate`, `fraudulent`, `requested_by_customer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountCapturable": 1,
      "amountReceived": 1,
      "canceledAt": 1,
      "cancellationReason": "string",
      "captureMethod": "string",
      "clientSecret": "string",
      "created": 1,
      "currency": "string",
      "description": "string",
      "id": "string",
      "latestCharge": "string",
      "object": "string",
      "paymentMethod": "string",
      "paymentMethodTypes": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountCapturable` | number |  |
| `amountReceived` | number |  |
| `canceledAt` | number |  |
| `cancellationReason` | string |  |
| `captureMethod` | string |  |
| `clientSecret` | string |  |
| `created` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | string |  |
| `latestCharge` | string |  |
| `object` | string |  |
| `paymentMethod` | string |  |
| `paymentMethodTypes` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `POST payment_intents/:intent/cancel` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-payment-intent.md) for the provider-specific parameters and requirements.


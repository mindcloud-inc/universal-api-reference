# Stripe: Create Payment Intent

Creates a new payment intent in Stripe.

```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-payment-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-payment-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-payment-intent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount intended to be collected, in the smallest currency unit. |
| `currency` | string | yes | Three-letter ISO currency code, in lowercase. |
| `customer` | string | no | Customer ID to attach to the PaymentIntent. |
| `paymentMethod` | string | no | PaymentMethod ID to attach to this PaymentIntent. |
| `description` | string | no | An arbitrary string attached to the object. |
| `confirm` | boolean | no | Set to true to attempt to confirm this PaymentIntent immediately. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `captureMethod` | list<string> | no | Controls when funds are captured from the customer. One of: `automatic`, `automatic_async`, `manual`. |

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

Through the native Stripe API, this operation is `POST payment_intents` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-intent.md) for the provider-specific parameters and requirements.


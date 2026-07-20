# Stripe: Get Payment Intent

Retrieves a payment intent from your Stripe account.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-payment-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-payment-intent?connectionId=$CONNECTION_ID&intent=pi_3MtwBwLkdIwHu7ix28a3tqPa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "intent": "pi_3MtwBwLkdIwHu7ix28a3tqPa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/get-payment-intent?${params}`, {
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
| `intent` | string | yes | PaymentIntent ID to retrieve (for example, pi_...). Example: `pi_3MtwBwLkdIwHu7ix28a3tqPa`. |

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

Through the native Stripe API, this operation is `GET payment_intents/:intent` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-intent.md) for the provider-specific parameters and requirements.


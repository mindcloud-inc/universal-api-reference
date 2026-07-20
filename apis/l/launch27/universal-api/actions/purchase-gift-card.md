# Launch27: Purchase Gift Card

Creates a new gift card purchase in Launch27.

```
POST https://connect.mindcloud.co/v1/universal/launch27/latest/actions/purchase-gift-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/purchase-gift-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipient_name": "Ava Chen",
  "recipient_email": "ava@example.com",
  "sender_name": "Ava Chen",
  "sender_email": "ava@example.com",
  "message": "string",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launch27/latest/actions/purchase-gift-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipient_name": "Ava Chen",
    "recipient_email": "ava@example.com",
    "sender_name": "Ava Chen",
    "sender_email": "ava@example.com",
    "message": "string",
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipient_name` | string | yes | Gift card recipient name. |
| `recipient_email` | string | yes | Gift card recipient email address. |
| `sender_name` | string | yes | Gift card sender name. |
| `sender_email` | string | yes | Gift card sender email address. |
| `message` | string | yes | Gift card message text. |
| `amount` | number | yes | Gift card amount. |
| `discount_code` | string | no | Optional gift card discount code. |
| `recaptcha_token` | string | no | Recaptcha token for gift card submission. |
| `fspay_payment_method_id` | string | no | FullSteam payment method ID for FSPay gift card purchases. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ga_item": {},
      "ga_transaction": {},
      "stripe_payment_intent_secret": "string",
      "stripe_requires_action": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ga_item` | object | Google Analytics item payload returned after a successful gift-card purchase. |
| `ga_transaction` | object | Google Analytics transaction payload returned after a successful gift-card purchase. |
| `stripe_payment_intent_secret` | string | Stripe payment intent secret used when additional action is required. |
| `stripe_requires_action` | boolean | Whether the Stripe gift-card purchase flow requires an additional customer action step. |

## Native endpoint

Through the native Launch27 API, this operation is `POST giftcard` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-gift-card.md) for the provider-specific parameters and requirements.


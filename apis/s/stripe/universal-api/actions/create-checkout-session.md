# Stripe: Create Checkout Session

Creates a new checkout session in Stripe.

```
POST https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-checkout-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mode": "payment"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripe/latest/actions/create-checkout-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mode": "payment"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | list<string> | yes | Checkout mode: payment, setup, or subscription. One of: `payment`, `setup`, `subscription`. Example: `payment`. |
| `lineItems[]` | array<object> | no | Line items for this checkout session. |
| `lineItems[].price` | string | no | The price ID for a line item. Example: `price_123`. |
| `lineItems[].quantity` | number | no | Quantity for the line item. Example: `1`. |
| `successUrl` | string | no | URL to redirect customers after successful checkout in hosted mode. Example: `https://example.com/success`. |
| `cancelUrl` | string | no | URL to redirect customers if they cancel checkout. Example: `https://example.com/cancel`. |
| `customer` | string | no | Existing customer ID to prefill checkout. Example: `cus_123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnUrl` | string | no | URL to return customers to your site for embedded/custom UI modes. Example: `https://example.com/return`. |
| `customerEmail` | string | no | Email used to prefill customer data when no customer ID is provided. Example: `customer@example.com`. |
| `paymentMethodTypes[]` | array<string> | no | Allowed payment method types for this session. Example: `card`. |
| `uiMode` | list<string> | no | Checkout UI mode: hosted, embedded, or custom. One of: `custom`, `embedded`, `hosted`. Example: `hosted`. |
| `clientReferenceId` | string | no | Reference ID to reconcile session with your internal systems. Example: `order_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountTotal": 1,
      "created": 1,
      "currency": "string",
      "customer": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "paymentStatus": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountTotal` | number | Total amount |
| `created` | number | Creation timestamp in seconds |
| `currency` | string | Session currency |
| `customer` | string | Customer ID |
| `id` | string | Checkout session ID |
| `mode` | string | Checkout mode |
| `object` | string | Stripe object type |
| `paymentStatus` | string | Payment status |
| `status` | string | Session status |
| `url` | string | Hosted checkout URL |

## Native endpoint

Through the native Stripe API, this operation is `POST checkout/sessions` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout-session.md) for the provider-specific parameters and requirements.


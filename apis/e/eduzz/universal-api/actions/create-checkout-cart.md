# Eduzz: Create Checkout Cart

Creates a checkout cart in Eduzz.

```
POST https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/create-checkout-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/create-checkout-cart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/create-checkout-cart', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.email` | string | no | Customer email address. |
| `customer.name` | string | no | Customer full name. |
| `items[].description` | string | no | Line item description shown in checkout. |
| `items[].price.currency` | string | no | Line item currency. |
| `items[].price.value` | string | no | Line item price value. |
| `items[].productId` | string | no | Product id to add to the cart. |
| `items[].quantity` | string | no | Line item quantity. |
| `orderId` | string | no | Your internal order reference. |
| `postbackUrl` | string | no | Webhook URL for cart events. |
| `returnUrl` | string | no | Buyer return URL after checkout. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `POST /sun/v1/cart` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout-cart.md) for the provider-specific parameters and requirements.


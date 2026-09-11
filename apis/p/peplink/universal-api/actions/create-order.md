# Peplink: Create Order



```
POST https://connect.mindcloud.co/v1/universal/peplink/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peplink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peplink/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerEmail": "ava@example.com",
  "orderItems[]": [
    "string"
  ],
  "orderItems[].sku": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peplink/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerEmail": "ava@example.com",
    "orderItems[]": ["string"],
    "orderItems[].sku": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingAddress` | object | no | Define a new billing address for this order. Make sure you set isUseDefaultBillingAddress to false when using new billing address. |
| `billingAddress.company` | string | no |  |
| `billingAddress.countryCode` | string | no | 2-char country code for this address. |
| `billingAddress.state` | string | no |  |
| `billingAddress.streetAddress` | string | no |  |
| `comment` | string | no | Add note for this order. |
| `customerEmail` | string | yes | Customer email to create the order. This should represent one of your users (seats) from your partner account. |
| `isUseDefaultBillingAddress` | boolean | no | true if to use the default billing address configured in eStore. false if you want to use a new billing address via billingAddress. |
| `orderItems[]` | array | yes | Ordered items in this order. Must contain at least one item. |
| `orderItems[].generateNewEsim` | boolean | no | Indicates if a new eSIM is needed to generate for the order item. Required if the order item is for generating new eSIM. |
| `orderItems[].iccids[]` | array | no | ICCIDs for the order item. Required if the order item is purchased for ICCIDs, e.g. data plan for eSIMs. |
| `orderItems[].quantity` | number | no | Defines how much quantity to purchase for the order item. Required if generateNewEsim is true. |
| `orderItems[].sku` | string | yes | SKU of the order item. |
| `paymentMethod` | string | no | Payment method for this order. Only payment terms PAYMENT_TERMS is supported now. |
| `billingAddress.city` | string | no |  |
| `isDryRun` | boolean | no | Set true if you want to test if your order is valid to create. false or leave it absent from the request if you want to create an actual order. |
| `couponCode` | string | no | Coupon code to apply discount to the order. |
| `orderItems[].serialNumbers[]` | array<string> | no |  |
| `billingAddress.zipCode` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Peplink API returns.

## Native endpoint

Through the native Peplink API, this operation is `POST orders` (base URL `https://portal.peplink.com/api/e/v1/cp/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.


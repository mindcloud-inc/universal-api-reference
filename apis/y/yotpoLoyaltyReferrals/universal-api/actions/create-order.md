# Yotpo Loyalty & Referrals: Create Order

Creates an order in Yotpo Loyalty & Referrals.

```
POST https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerEmail": "ava@example.com",
  "totalAmountCents": 1,
  "currencyCode": "string",
  "orderId": "string",
  "ipAddress": "string",
  "userAgent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerEmail": "ava@example.com",
    "totalAmountCents": 1,
    "currencyCode": "string",
    "orderId": "string",
    "ipAddress": "string",
    "userAgent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerEmail` | string | yes | The customer's email address. |
| `totalAmountCents` | number | yes | The order total in cents. |
| `currencyCode` | string | yes | The ISO currency code for the order. |
| `orderId` | string | yes | The merchant order identifier. |
| `ipAddress` | string | yes | The customer's IP address. |
| `userAgent` | string | yes | The customer's browser or device user agent. |
| `customerId` | string | no | The identifier used to uniquely identify the customer in your system. |
| `status` | string | no | Order status used to determine how Yotpo should process rewards and discount removal. |
| `createdAt` | string | no | Timestamp describing when this order was placed. |
| `couponCode` | string | no | Comma-separated list of coupon codes used on the order. |
| `ignoreIpUa` | boolean | no | Ignore IP address and user-agent fraud checks for this order. |
| `discountAmountCents` | number | no | Total discount amount applied to the order in cents. |
| `tags` | string | no | Comma-separated list of order tags. |
| `clerkEmployeeId` | string | no | Employee ID of the store clerk who processed the transaction. |
| `clerkName` | string | no | Name of the store clerk who processed the transaction. |
| `storeAddress` | string | no | Street address of the store location for the order. |
| `storeCity` | string | no | City of the store location for the order. |
| `storeState` | string | no | State or province of the store location for the order. |
| `channelType` | string | no | Order channel, such as online or offline. |
| `items[].id` | string | no | Unique identifier of a purchased product line item. |
| `items[].name` | string | no | Customer-facing product name for a purchased item. |
| `items[].quantity` | number | no | Quantity purchased for the item. |
| `items[].priceCents` | number | no | Unit price for the item in cents. |
| `items[].collections` | string | no | Comma-separated collections or tags for the item. |
| `items[].type` | string | no | Product category or type for the purchased item. |
| `items[].vendor` | string | no | Vendor or manufacturer for the purchased item. |
| `customer.tags` | string | no | Comma-separated customer tags. Include this if customer-based include or exclude rules are configured. |
| `customer.hasAccount` | boolean | no | Whether the customer has an account with the ecommerce platform. |
| `customer.optedIn` | boolean | no | Whether the customer should be opted in to the loyalty program. |
| `customer.optedInAt` | string | no | Timestamp when the customer opted in to the loyalty program. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yotpo Loyalty & Referrals API returns.

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/orders` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.


# Order Desk: Create Order

Creates a new order in Order Desk.

```
POST https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "shipping.firstName": "Ava",
  "shipping.lastName": "Chen",
  "shipping.address1": "string",
  "shipping.city": "string",
  "shipping.state": "string",
  "shipping.postalCode": "string",
  "shipping.country": "string",
  "customer.firstName": "Ava",
  "customer.lastName": "Chen",
  "customer.address1": "string",
  "customer.city": "string",
  "customer.state": "string",
  "customer.postalCode": "string",
  "customer.country": "string",
  "orderItems[].name": "Ava Chen",
  "orderItems[].price": 1,
  "orderItems[].quantity": 1,
  "orderItems[].code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "shipping.firstName": "Ava",
    "shipping.lastName": "Chen",
    "shipping.address1": "string",
    "shipping.city": "string",
    "shipping.state": "string",
    "shipping.postalCode": "string",
    "shipping.country": "string",
    "customer.firstName": "Ava",
    "customer.lastName": "Chen",
    "customer.address1": "string",
    "customer.city": "string",
    "customer.state": "string",
    "customer.postalCode": "string",
    "customer.country": "string",
    "orderItems[].name": "Ava Chen",
    "orderItems[].price": 1,
    "orderItems[].quantity": 1,
    "orderItems[].code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Customer email address. |
| `shippingMethod` | string | no | Shipping method label. |
| `shipping.firstName` | string | yes | Shipping first name. |
| `shipping.lastName` | string | yes | Shipping last name. |
| `shipping.address1` | string | yes | Shipping street address. |
| `shipping.city` | string | yes | Shipping city. |
| `shipping.state` | string | yes | Shipping state or region. |
| `shipping.postalCode` | string | yes | Shipping postal code. |
| `shipping.country` | string | yes | Shipping country code or full country name. |
| `customer.firstName` | string | yes | Customer first name. |
| `customer.lastName` | string | yes | Customer last name. |
| `customer.address1` | string | yes | Customer street address. |
| `customer.city` | string | yes | Customer city. |
| `customer.state` | string | yes | Customer state or region. |
| `customer.postalCode` | string | yes | Customer postal code. |
| `customer.country` | string | yes | Customer country code or full country name. |
| `orderItems[].name` | string | yes | Order item name. |
| `orderItems[].price` | number | yes | Order item unit price. |
| `orderItems[].quantity` | number | yes | Order item quantity. |
| `orderItems[].code` | string | yes | Order item SKU or code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {},
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "discountTotal": 1,
      "email": "ava@example.com",
      "folderId": 1,
      "id": "string",
      "orderItems": [
        {}
      ],
      "orderTotal": 1,
      "productTotal": 1,
      "quantityTotal": 1,
      "shipping": {},
      "shippingMethod": "string",
      "shippingTotal": 1,
      "sourceName": "Ava Chen",
      "taxTotal": 1,
      "weightTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object | Customer address details. |
| `dateAdded` | date | Order creation timestamp in UTC. |
| `dateUpdated` | date | Last update timestamp in UTC. |
| `discountTotal` | number | Discount total. |
| `email` | string | Customer email address. |
| `folderId` | number | Current folder ID. |
| `id` | string | Order Desk internal order ID. |
| `orderItems` | array<object> | Order line items. |
| `orderTotal` | number | Final order total. |
| `productTotal` | number | Product subtotal. |
| `quantityTotal` | number | Total quantity across order items. |
| `shipping` | object | Shipping address details. |
| `shippingMethod` | string | Shipping method name. |
| `shippingTotal` | number | Shipping total. |
| `sourceName` | string | Order source name. |
| `taxTotal` | number | Tax total. |
| `weightTotal` | number | Total order weight. |

## Native endpoint

Through the native Order Desk API, this operation is `POST /orders` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.


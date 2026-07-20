# MailBluster: Create Order

Creates a new order in MailBluster.

```
POST https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "customer": {},
  "currency": "string",
  "totalPrice": 1,
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "customer": {},
    "currency": "string",
    "totalPrice": 1,
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Unique order ID in MailBluster. |
| `customer` | object | yes | Customer object for the order, including email and optional name/subscription fields. |
| `currency` | string | yes | Order currency code, such as USD. |
| `totalPrice` | number | yes | Total price of the order. |
| `items[]` | array<object> | yes | Array of products included in the order. |
| `campaignId` | number | no | Optional campaign ID to associate with the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "order": {
        "campaign": {},
        "createdAt": "string",
        "currency": "string",
        "id": "string",
        "lead": {
          "email": "ava@example.com",
          "fullName": "Ava Chen",
          "id": 1
        },
        "orderItems": [
          {
            "price": "string",
            "product": {
              "id": "string",
              "name": "Ava Chen"
            },
            "quantity": 1,
            "totalPrice": "string"
          }
        ],
        "totalPrice": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Operation result message. |
| `order` | object | Created order. |
| `order.campaign` | object | Associated campaign when present. |
| `order.createdAt` | string | Creation timestamp. |
| `order.currency` | string | Order currency. |
| `order.id` | string | Order ID. |
| `order.lead` | object | Lead associated with the order. |
| `order.lead.email` | string | Lead email address. |
| `order.lead.fullName` | string | Lead full name. |
| `order.lead.id` | number | Lead ID. |
| `order.orderItems` | array<object> | Order line items. |
| `order.orderItems[].price` | string | Item price. |
| `order.orderItems[].product` | object | Line item product. |
| `order.orderItems[].product.id` | string | Product ID. |
| `order.orderItems[].product.name` | string | Product name. |
| `order.orderItems[].quantity` | number | Item quantity. |
| `order.orderItems[].totalPrice` | string | Line total. |
| `order.totalPrice` | string | Order total price. |
| `order.updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `POST /orders` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.


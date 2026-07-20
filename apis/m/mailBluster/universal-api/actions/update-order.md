# MailBluster: Update Order

Updates an existing order in MailBluster.

```
PUT https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Unique order ID to update. |
| `customer` | object | no | Updated customer object for the order. |
| `currency` | string | no | Updated order currency code. |
| `totalPrice` | number | no | Updated total price of the order. |
| `items[]` | array<object> | no | Updated array of products included in the order. |
| `campaignId` | number | no | Updated optional campaign ID to associate with the order. |

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
| `order` | object | Updated order. |
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

Through the native MailBluster API, this operation is `PUT /orders/:orderId` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.


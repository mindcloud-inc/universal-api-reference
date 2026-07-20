# MailBluster: Get Order

Retrieves an order from MailBluster.

```
GET https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | Unique order ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object | Associated campaign when present. |
| `createdAt` | string | Creation timestamp. |
| `currency` | string | Order currency. |
| `id` | string | Order ID. |
| `lead` | object | Lead associated with the order. |
| `lead.email` | string | Lead email address. |
| `lead.fullName` | string | Lead full name. |
| `lead.id` | number | Lead ID. |
| `orderItems` | array<object> | Order line items. |
| `orderItems[].price` | string | Item price. |
| `orderItems[].product` | object | Line item product. |
| `orderItems[].product.id` | string | Product ID. |
| `orderItems[].product.name` | string | Product name. |
| `orderItems[].quantity` | number | Item quantity. |
| `orderItems[].totalPrice` | string | Line total. |
| `totalPrice` | string | Order total price. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `GET /orders/:orderId` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.


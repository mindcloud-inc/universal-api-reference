# MailBluster: List Orders

Retrieves a page of orders from MailBluster.

```
GET https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-orders?${params}`, {
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
| `pageNo` | number | no | Page number to retrieve. Default: `1`. |
| `perPage` | number | no | Number of orders to retrieve per page. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "nextPageNo": 1,
        "pageNo": 1,
        "perPage": 1,
        "prevPageNo": 1,
        "total": 1,
        "totalPage": 1
      },
      "orders": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object | Pagination metadata. |
| `meta.nextPageNo` | number | Next page number when available. |
| `meta.pageNo` | number | Current page number. |
| `meta.perPage` | number | Orders per page. |
| `meta.prevPageNo` | number | Previous page number when available. |
| `meta.total` | number | Total number of orders. |
| `meta.totalPage` | number | Total number of pages. |
| `orders` | array<object> | Orders in the requested page. |
| `orders[].campaign` | object | Associated campaign when present. |
| `orders[].createdAt` | string | Creation timestamp. |
| `orders[].currency` | string | Order currency. |
| `orders[].id` | string | Order ID. |
| `orders[].lead` | object | Lead associated with the order. |
| `orders[].lead.email` | string | Lead email address. |
| `orders[].lead.fullName` | string | Lead full name. |
| `orders[].lead.id` | number | Lead ID. |
| `orders[].orderItems` | array<object> | Order line items. |
| `orders[].orderItems[].price` | string | Item price. |
| `orders[].orderItems[].product` | object | Line item product. |
| `orders[].orderItems[].product.id` | string | Product ID. |
| `orders[].orderItems[].product.name` | string | Product name. |
| `orders[].orderItems[].quantity` | number | Item quantity. |
| `orders[].orderItems[].totalPrice` | string | Line total. |
| `orders[].totalPrice` | string | Order total price. |
| `orders[].updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `GET /orders` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.


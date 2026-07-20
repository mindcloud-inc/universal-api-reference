# Sellty: Get Order



```
GET https://connect.mindcloud.co/v1/universal/sellty/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sellty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sellty/latest/actions/get-order?connectionId=$CONNECTION_ID&order=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sellty/latest/actions/get-order?${params}`, {
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
| `order` | string | yes | Order number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "comment": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "delivery": true,
      "email": "ava@example.com",
      "export1c": true,
      "id": 1,
      "is_paid": true,
      "new_status": true,
      "number": 1,
      "order_status": {},
      "order_status_id": 1,
      "payment_method": "string",
      "products": [
        "string"
      ],
      "seller_id": 1,
      "status": 1,
      "store_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Delivery address. |
| `comment` | string | Order comment. |
| `created_at` | date | Order creation timestamp. |
| `delivery` | boolean | Whether delivery is enabled for the order. |
| `email` | string | Customer email. |
| `export1c` | boolean | Whether the order is marked for 1C export. |
| `id` | number | Order ID. |
| `is_paid` | boolean | Whether the order is paid. |
| `new_status` | boolean | Whether the order has a new status. |
| `number` | number | Order number. |
| `order_status` | object | Order status details. |
| `order_status_id` | number | Order status ID. |
| `payment_method` | string | Payment method. |
| `products` | array<string> | Order products. |
| `seller_id` | number | Seller ID. |
| `status` | number | Order status value. |
| `store_id` | number | Store ID. |
| `updated_at` | date | Order update timestamp. |

## Native endpoint

Through the native Sellty API, this operation is `POST /seller/api/v-1-0/get-order/{order}` (base URL `https://my.sellty.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.


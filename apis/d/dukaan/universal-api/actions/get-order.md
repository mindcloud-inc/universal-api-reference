# Dukaan: Get Order

Retrieves an order from Dukaan.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/get-order?connectionId=$CONNECTION_ID&orderUuid=order-uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderUuid": "order-uuid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/get-order?${params}`, {
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
| `orderUuid` | string | yes | Dukaan order UUID. Example: `order-uuid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyer_address": {},
      "coupon_discount": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "delivery_cost": 1,
      "display_order_id": "string",
      "id": 1,
      "is_new": true,
      "line_items": [
        {}
      ],
      "modified_at": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "payment_mode": 1,
      "product_count": 1,
      "status": 1,
      "total_cost": 1,
      "type": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyer_address` | object | Buyer address details |
| `coupon_discount` | number | Coupon discount amount |
| `created_at` | date | Creation timestamp |
| `delivery_cost` | number | Delivery charge |
| `display_order_id` | string | Human-readable order ID |
| `id` | number | Dukaan order ID |
| `is_new` | boolean | Whether the order is new |
| `line_items` | array<object> | Order line items |
| `modified_at` | date | Last modified timestamp |
| `notes` | string | Order notes |
| `payment_mode` | number | Payment mode code |
| `product_count` | number | Number of products in the order |
| `status` | number | Order status code |
| `total_cost` | number | Order total cost |
| `type` | number | Order type code |
| `uuid` | string | Dukaan order UUID |

## Native endpoint

Through the native Dukaan API, this operation is `GET api/order/seller/:orderUuid/order/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.


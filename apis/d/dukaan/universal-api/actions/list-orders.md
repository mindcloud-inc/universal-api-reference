# Dukaan: List Orders

Retrieves orders from Dukaan.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-orders?${params}`, {
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
| `createdAtAfter` | date | no | Lower bound order creation date. Example: `2024-02-05`. |
| `createdAtBefore` | date | no | Upper bound order creation date. Example: `2024-02-12`. |

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

Through the native Dukaan API, this operation is `GET api/seller-front/order-list/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.


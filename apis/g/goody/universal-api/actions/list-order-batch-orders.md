# Goody: List Order Batch Orders

Retrieves orders for an order batch in Goody.

```
GET https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-order-batch-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-order-batch-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-order-batch-orders?${params}`, {
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
| `id` | string | yes | Order batch ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amounts": {
        "amount_global_relay_cost": "string",
        "amount_pre_tax_total": 1,
        "amount_processing_fee": 1,
        "amount_product": 1,
        "amount_shipping": 1,
        "amount_tax": "string",
        "amount_total": "string"
      },
      "card_id": "string",
      "cart": {
        "id": "string",
        "items": {
          "id": "string",
          "product": {
            "brand": {},
            "id": "string",
            "name": "Ava Chen"
          },
          "quantity": 1
        }
      },
      "expires_at": "string",
      "id": "string",
      "individual_gift_link": "https://example.com",
      "is_swapped": true,
      "message": "string",
      "order_batch_id": "string",
      "original_amounts": "string",
      "original_cart": "string",
      "recipient_email": "ava@example.com",
      "recipient_first_name": "Ava",
      "recipient_last_name": "Chen",
      "reference_id": "string",
      "sender": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "last_name": "Chen"
      },
      "shipments": [
        "string"
      ],
      "status": "string",
      "thank_you_note": "string",
      "view_count_recipient": 1,
      "workspace_id": "string",
      "workspace_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amounts` | object |  |
| `amounts.amount_global_relay_cost` | string |  |
| `amounts.amount_pre_tax_total` | number |  |
| `amounts.amount_processing_fee` | number |  |
| `amounts.amount_product` | number |  |
| `amounts.amount_shipping` | number |  |
| `amounts.amount_tax` | string |  |
| `amounts.amount_total` | string |  |
| `card_id` | string |  |
| `cart` | object |  |
| `cart.id` | string |  |
| `cart.items` | array<object> |  |
| `cart.items.id` | string |  |
| `cart.items.product` | object |  |
| `cart.items.product.brand` | object |  |
| `cart.items.product.id` | string |  |
| `cart.items.product.name` | string |  |
| `cart.items.quantity` | number |  |
| `expires_at` | string |  |
| `id` | string |  |
| `individual_gift_link` | string |  |
| `is_swapped` | boolean |  |
| `message` | string |  |
| `order_batch_id` | string |  |
| `original_amounts` | string |  |
| `original_cart` | string |  |
| `recipient_email` | string |  |
| `recipient_first_name` | string |  |
| `recipient_last_name` | string |  |
| `reference_id` | string |  |
| `sender` | object |  |
| `sender.email` | string |  |
| `sender.first_name` | string |  |
| `sender.last_name` | string |  |
| `shipments` | array<string> |  |
| `status` | string |  |
| `thank_you_note` | string |  |
| `view_count_recipient` | number |  |
| `workspace_id` | string |  |
| `workspace_name` | string |  |

## Native endpoint

Through the native Goody API, this operation is `GET /v1/order_batches/:id/orders` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-order-batch-orders.md) for the provider-specific parameters and requirements.


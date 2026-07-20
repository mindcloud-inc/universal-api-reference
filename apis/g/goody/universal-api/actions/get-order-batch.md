# Goody: Get Order Batch

Retrieves an order batch from Goody.

```
GET https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-order-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-order-batch?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-order-batch?${params}`, {
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
      "from_name": "Ava Chen",
      "id": "string",
      "message": "string",
      "orders_count": 1,
      "orders_preview": {
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
            "product": {},
            "quantity": 1
          }
        },
        "expires_at": "string",
        "id": "string",
        "individual_gift_link": "https://example.com",
        "is_swapped": true,
        "message": "string",
        "order_batch_id": "string",
        "recipient_email": "ava@example.com",
        "recipient_first_name": "Ava",
        "recipient_last_name": "Chen",
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
      },
      "send_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from_name` | string |  |
| `id` | string |  |
| `message` | string |  |
| `orders_count` | number |  |
| `orders_preview` | array<object> |  |
| `orders_preview.amounts` | object |  |
| `orders_preview.amounts.amount_global_relay_cost` | string |  |
| `orders_preview.amounts.amount_pre_tax_total` | number |  |
| `orders_preview.amounts.amount_processing_fee` | number |  |
| `orders_preview.amounts.amount_product` | number |  |
| `orders_preview.amounts.amount_shipping` | number |  |
| `orders_preview.amounts.amount_tax` | string |  |
| `orders_preview.amounts.amount_total` | string |  |
| `orders_preview.card_id` | string |  |
| `orders_preview.cart` | object |  |
| `orders_preview.cart.id` | string |  |
| `orders_preview.cart.items` | array<object> |  |
| `orders_preview.cart.items.id` | string |  |
| `orders_preview.cart.items.product` | object |  |
| `orders_preview.cart.items.quantity` | number |  |
| `orders_preview.expires_at` | string |  |
| `orders_preview.id` | string |  |
| `orders_preview.individual_gift_link` | string |  |
| `orders_preview.is_swapped` | boolean |  |
| `orders_preview.message` | string |  |
| `orders_preview.order_batch_id` | string |  |
| `orders_preview.recipient_email` | string |  |
| `orders_preview.recipient_first_name` | string |  |
| `orders_preview.recipient_last_name` | string |  |
| `orders_preview.sender` | object |  |
| `orders_preview.sender.email` | string |  |
| `orders_preview.sender.first_name` | string |  |
| `orders_preview.sender.last_name` | string |  |
| `orders_preview.shipments` | array<string> |  |
| `orders_preview.status` | string |  |
| `orders_preview.thank_you_note` | string |  |
| `orders_preview.view_count_recipient` | number |  |
| `orders_preview.workspace_id` | string |  |
| `orders_preview.workspace_name` | string |  |
| `send_status` | string |  |

## Native endpoint

Through the native Goody API, this operation is `GET /v1/order_batches/:id` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-batch.md) for the provider-specific parameters and requirements.


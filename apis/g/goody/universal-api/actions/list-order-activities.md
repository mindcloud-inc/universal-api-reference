# Goody: List Order Activities

Retrieves order activities from Goody.

```
GET https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-order-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-order-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goody/latest/actions/list-order-activities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "order": {
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
        "original_amounts": "string",
        "original_cart": "string",
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
      "order_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `order` | object |  |
| `order_status` | string |  |
| `order.amounts` | object |  |
| `order.amounts.amount_global_relay_cost` | string |  |
| `order.amounts.amount_pre_tax_total` | number |  |
| `order.amounts.amount_processing_fee` | number |  |
| `order.amounts.amount_product` | number |  |
| `order.amounts.amount_shipping` | number |  |
| `order.amounts.amount_tax` | string |  |
| `order.amounts.amount_total` | string |  |
| `order.card_id` | string |  |
| `order.cart` | object |  |
| `order.cart.id` | string |  |
| `order.cart.items` | array<object> |  |
| `order.cart.items.id` | string |  |
| `order.cart.items.product` | object |  |
| `order.cart.items.quantity` | number |  |
| `order.expires_at` | string |  |
| `order.id` | string |  |
| `order.individual_gift_link` | string |  |
| `order.is_swapped` | boolean |  |
| `order.message` | string |  |
| `order.order_batch_id` | string |  |
| `order.original_amounts` | string |  |
| `order.original_cart` | string |  |
| `order.recipient_email` | string |  |
| `order.recipient_first_name` | string |  |
| `order.recipient_last_name` | string |  |
| `order.sender` | object |  |
| `order.sender.email` | string |  |
| `order.sender.first_name` | string |  |
| `order.sender.last_name` | string |  |
| `order.shipments` | array<string> |  |
| `order.status` | string |  |
| `order.thank_you_note` | string |  |
| `order.view_count_recipient` | number |  |
| `order.workspace_id` | string |  |
| `order.workspace_name` | string |  |

## Native endpoint

Through the native Goody API, this operation is `GET /v1/order_activities` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-activities.md) for the provider-specific parameters and requirements.


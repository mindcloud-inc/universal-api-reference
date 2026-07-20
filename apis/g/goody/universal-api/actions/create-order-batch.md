# Goody: Create Order Batch

Creates a new order batch in Goody.

```
POST https://connect.mindcloud.co/v1/universal/goody/latest/actions/create-order-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goody/latest/actions/create-order-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromName": "Ava Chen",
  "recipients[]": [
    {}
  ],
  "cart": {},
  "sendMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goody/latest/actions/create-order-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromName": "Ava Chen",
    "recipients[]": [{}],
    "cart": {},
    "sendMethod": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromName` | string | yes | The name of the sender of the order (typically a gift), to be displayed as "from". |
| `message` | string | no | For gifts, a message for the gift to be displayed in the digital unwrapping and email notifications, if enabled. |
| `recipients[]` | array<object> | yes |  |
| `cart` | object | yes |  |
| `sendMethod` | string | yes | The method for sending a order batch. `email_and_link` sends a gift email to the recipient (specify `email` for each recipient). `link_multiple_custom_list` generates a gift link without an automatic email. `direct_send` ships the product directly to the recipient (specify `mailing_address` for each recipient). For more information, see [Send Methods](/introduction/send-methods). |
| `cardId` | string | no | The digital greeting card to attach to gifts. A card must be specified if a message is specified, since the message is displayed after the card is opened. |
| `paymentMethodId` | string | no | The payment method used to pay for this order batch. If not specified, defaults to the first payment method on the account. If the account has no payment methods, then the order batch creation will fail. |
| `workspaceId` | string | no | Workspace to create the order batch in. If not specified, creates the order batch in the oldest workspace the user has access to. |
| `scheduledSendOn` | date | no | The date and time at which the order batch will be sent. If not specified, the order batch is sent immediately. If an order batch is scheduled to be sent in the future, then orders will not be created until the scheduled send time. ISO 8601 format. |
| `expiresAt` | date | no | The date and time at which the order batch will expire. If not specified, the order batch does not expire. An expiry must be set for orders paid using account balance. ISO 8601 format. |
| `swap` | string | no | What method to use to allow recipients to swap their gift. `single` (default) allows the recipient to swap the gift for one item, with hidden gift prices. `multiple` allows them to swap for multiple items up to the gift cost, with gift prices shown. `disabled` disables swapping on the gift. For gift collections (gift of choice), this must not be `disabled`. |
| `internationalShippingTier` | string | no | Whether to enable international shipping on this order. `disabled` (default) only enables US shipping on this order. `standard` combined with `international_gift_cards_enabled` enables international gift cards. `full` enables the full global catalog for 100+ countries, with additional tax, duties, and freight costs. |
| `internationalGiftCardsEnabled` | boolean | no | Whether to enable international gift cards on this order. If `true` and the `international_shipping_tier` is `standard`, then international gift cards can be swapped to. If `false`, then international gift cards are not available to be swapped to. |
| `notificationsEnabled` | boolean | no | Direct Send only. Whether to enable notifications for Direct Send orders. If `true`, we send confirmation and shipping notifications to Direct Send recipients. If `false`, we do not send any notifications to Direct Send recipients. |
| `reservedOptions` | object | no | For approved API partners only. |

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

Through the native Goody API, this operation is `POST /v1/order_batches` (base URL `https://api.ongoody.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-batch.md) for the provider-specific parameters and requirements.


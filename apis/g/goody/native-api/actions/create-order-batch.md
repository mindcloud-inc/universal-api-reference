# Create Order Batch with Goody

Creates a new order batch in Goody.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/order_batches`
- **Base URL:** `https://api.ongoody.com`
- **Official documentation:** [Create Order Batch](https://developer.ongoody.com/api-reference/order-batches/create-an-order-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_name` | body | `string` | yes | The name of the sender of the order (typically a gift), to be displayed as "from". |
| `message` | body | `string` | no | For gifts, a message for the gift to be displayed in the digital unwrapping and email notifications, if enabled. |
| `recipients[]` | body | `array<object>` | yes | — |
| `cart` | body | `object` | yes | — |
| `send_method` | body | `string` | yes | The method for sending a order batch. `email_and_link` sends a gift email to the recipient (specify `email` for each recipient). `link_multiple_custom_list` generates a gift link without an automatic email. `direct_send` ships the product directly to the recipient (specify `mailing_address` for each recipient). For more information, see [Send Methods](/introduction/send-methods). |
| `card_id` | body | `string` | no | The digital greeting card to attach to gifts. A card must be specified if a message is specified, since the message is displayed after the card is opened. |
| `payment_method_id` | body | `string` | no | The payment method used to pay for this order batch. If not specified, defaults to the first payment method on the account. If the account has no payment methods, then the order batch creation will fail. |
| `workspace_id` | body | `string` | no | Workspace to create the order batch in. If not specified, creates the order batch in the oldest workspace the user has access to. |
| `scheduled_send_on` | body | `date` | no | The date and time at which the order batch will be sent. If not specified, the order batch is sent immediately. If an order batch is scheduled to be sent in the future, then orders will not be created until the scheduled send time. ISO 8601 format. |
| `expires_at` | body | `date` | no | The date and time at which the order batch will expire. If not specified, the order batch does not expire. An expiry must be set for orders paid using account balance. ISO 8601 format. |
| `swap` | body | `string` | no | What method to use to allow recipients to swap their gift. `single` (default) allows the recipient to swap the gift for one item, with hidden gift prices. `multiple` allows them to swap for multiple items up to the gift cost, with gift prices shown. `disabled` disables swapping on the gift. For gift collections (gift of choice), this must not be `disabled`. |
| `international_shipping_tier` | body | `string` | no | Whether to enable international shipping on this order. `disabled` (default) only enables US shipping on this order. `standard` combined with `international_gift_cards_enabled` enables international gift cards. `full` enables the full global catalog for 100+ countries, with additional tax, duties, and freight costs. |
| `international_gift_cards_enabled` | body | `boolean` | no | Whether to enable international gift cards on this order. If `true` and the `international_shipping_tier` is `standard`, then international gift cards can be swapped to. If `false`, then international gift cards are not available to be swapped to. |
| `notifications_enabled` | body | `boolean` | no | Direct Send only. Whether to enable notifications for Direct Send orders. If `true`, we send confirmation and shipping notifications to Direct Send recipients. If `false`, we do not send any notifications to Direct Send recipients. |
| `reserved_options` | body | `object` | no | For approved API partners only. |

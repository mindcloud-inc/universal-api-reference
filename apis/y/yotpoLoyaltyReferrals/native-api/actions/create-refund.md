# Create Refund with Yotpo Loyalty & Referrals

Creates a refund in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/refunds`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Create Refund](https://loyaltyapi.yotpo.com/reference/create-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `string` | yes | The order identifier being refunded. |
| `total_amount_cents` | body | `number` | yes | The refund total in cents. |
| `id` | body | `string` | no | Unique identifier for the refund in your system. |
| `currency` | body | `string` | no | Refund currency code. Required when using multi-currency. |
| `items[].id` | body | `string` | no | Identifier of a refunded line item. Must match the item ID used when the order was created. |
| `items[].quantity` | body | `number` | no | Quantity refunded for the line item. |

# Create Refund Quote with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders/:order_id/payment_actions/refund_quotes`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes |
| `items[].item_type` | body | `string<object>` | yes |
| `items[].reason` | body | `string<object>` | no |
| `order_id` | path | `string` | yes |
| `items[].amount` | body | `number<object>` | yes |
| `items[].item_id` | body | `number<object>` | yes |

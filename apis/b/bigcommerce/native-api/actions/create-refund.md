# Create Refund with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders/:order_id/payment_actions/refunds`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes | — |
| `items[].item_type` | body | `string<object>` | yes | — |
| `payments[].provider_id` | body | `string<object>` | no | — |
| `items[].reason` | body | `string<object>` | no | — |
| `order_id` | path | `string` | yes | — |
| `payments[].amount` | body | `number<object>` | no | — |
| `items[].amount` | body | `number<object>` | yes | — |
| `payments[]` | body | `array<object>` | no | — |
| `payments[].offline` | body | `boolean<object>` | no | Whether the payment was marked as offline or performed through an online payment service. Example: true |
| `items[].item_id` | body | `number<object>` | yes | — |

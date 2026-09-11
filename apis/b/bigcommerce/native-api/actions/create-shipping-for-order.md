# Create Shipping For Order with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/orders/:order_id/shipments`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `items[].quantity` | body | `number` | no |
| `tracking_number` | body | `string` | no |
| `items[].order_product_id` | body | `string` | no |
| `shipping_provider` | body | `string` | no |
| `order_id` | path | `string` | yes |
| `order_address_id` | body | `string` | yes |
| `items[]` | body | `array<object>` | yes |

# Fulfil Order with Stockpilot

Updates an order as fulfilled in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/fulfil`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Fulfil Order](https://api.stockpilot.dev/redoc#operation/fulfil_order_orders_fulfil_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `carrier_code` | body | `string` | no |
| `items[].sku` | body | `string` | no |
| `order_pk` | body | `number` | no |
| `service` | body | `string` | no |
| `shipment_type` | body | `string` | no |
| `shipping_method` | body | `string` | no |
| `order_number` | body | `string` | no |
| `fulfilled_at` | body | `string` | no |
| `carrier_name` | body | `string` | no |
| `tracking_code` | body | `string` | no |
| `tracking_url` | body | `string` | no |
| `items[]` | body | `array<object>` | no |
| `items[].quantity` | body | `number` | no |

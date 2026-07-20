# Create Order with Stockpilot

Creates a new order in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/create`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Create Order](https://api.stockpilot.dev/redoc#operation/create_order_orders_create_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address_2` | body | `string` | no |
| `address_2` | body | `string` | no |
| `billing` | body | `object` | yes |
| `billing.city` | body | `string` | no |
| `billing.company` | body | `string` | no |
| `billing.region` | body | `string` | no |
| `billing.street` | body | `string` | no |
| `billing.suffix` | body | `string` | no |
| `customer_note` | body | `string` | no |
| `customer_phone` | body | `string` | no |
| `housenumber` | body | `string` | no |
| `housenumber` | body | `string` | no |
| `shipping_method` | body | `string` | no |
| `shipping_total` | body | `string` | no |
| `shipping.city` | body | `string` | no |
| `shipping.company` | body | `string` | no |
| `shipping.region` | body | `string` | no |
| `shipping.street` | body | `string` | no |
| `shipping.suffix` | body | `string` | no |
| `vat_number` | body | `string` | no |
| `billing.firstname` | body | `string` | yes |
| `billing.lastname` | body | `string` | yes |
| `billing.zipcode` | body | `string` | yes |
| `billing.country` | body | `string` | yes |
| `shipping` | body | `object` | yes |
| `shipping.firstname` | body | `string` | yes |
| `shipping.lastname` | body | `string` | yes |
| `shipping.zipcode` | body | `string` | yes |
| `shipping.country` | body | `string` | yes |
| `customer_email` | body | `string` | yes |
| `line_items[]` | body | `array<object>` | yes |
| `line_items[].product_id` | body | `string` | yes |
| `line_items[].price` | body | `string` | yes |
| `line_items[].quantity` | body | `number` | yes |

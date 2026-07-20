# Create Sales Order with Katana

Creates a new sales order in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/sales_orders`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Sales Order](https://developer.katanamrp.com/reference/create-sales-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_no` | body | `string` | yes | — |
| `customer_id` | body | `number` | yes | — |
| `sales_order_rows[]` | body | `array<object>` | yes | — |
| `sales_order_rows[].quantity` | body | `number` | yes | — |
| `sales_order_rows[].variant_id` | body | `number` | yes | — |
| `sales_order_rows[].tax_rate_id` | body | `number` | no | — |
| `sales_order_rows[].location_id` | body | `number` | no | — |
| `sales_order_rows[].attributes[]` | body | `array<object>` | no | — |
| `sales_order_rows[].attributes[].key` | body | `string` | no | — |
| `sales_order_rows[].attributes[].value` | body | `string` | no | — |
| `sales_order_rows[].price_per_unit` | body | `number` | no | — |
| `sales_order_rows[].total_discount` | body | `number` | no | — |
| `tracking_number` | body | `string` | no | Maximum length: 256. |
| `tracking_number_url` | body | `string` | no | Maximum length: 2048. |
| `addresses[]` | body | `array<object>` | no | — |
| `addresses[].entity_type` | body | `string` | no | — |
| `addresses[].first_name` | body | `string` | no | — |
| `addresses[].last_name` | body | `string` | no | — |
| `addresses[].company` | body | `string` | no | — |
| `addresses[].phone` | body | `string` | no | — |
| `addresses[].line_1` | body | `string` | no | — |
| `addresses[].line_2` | body | `string` | no | — |
| `addresses[].city` | body | `string` | no | — |
| `addresses[].state` | body | `string` | no | — |
| `addresses[].zip` | body | `string` | no | — |
| `addresses[].country` | body | `string` | no | — |
| `order_created_date` | body | `string` | no | — |
| `delivery_date` | body | `string` | no | — |
| `currency` | body | `string` | no | E.g. USD, EUR. All currently active currency codes in ISO 4217 format. |
| `location_id` | body | `number` | no | — |
| `status` | body | `string` | no | When the status is omitted, NOT_SHIPPED is used as default.         Use PENDING when you want to create sales order quotes. |
| `additional_info` | body | `string` | no | — |
| `customer_ref` | body | `string` | no | Maximum length: 255. |
| `ecommerce_order_type` | body | `string` | no | — |
| `ecommerce_store_name` | body | `string` | no | — |
| `ecommerce_order_id` | body | `string` | no | — |

# Create Order with WooCommerce

Creates a new order in WooCommerce.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `{siteUrl}/wp-json/wc/v3`
- **Official documentation:** [Create Order](https://woocommerce.github.io/woocommerce-rest-api-docs/#create-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `list<string>` | no | Order status such as pending, processing, completed, or cancelled. Accepted values: `cancelled`, `completed`, `failed`, `on-hold`, `pending`, `processing`, `refunded`, `trash`. |
| `set_paid` | body | `boolean` | no | Whether the order should be marked paid immediately. |
| `customer_id` | body | `list<number>` | no | Numeric ID of the existing customer for the order. |
| `payment_method` | body | `string` | no | — |
| `payment_method_title` | body | `string` | no | — |
| `billing` | body | `object` | no | — |
| `billing.first_name` | body | `string` | no | — |
| `billing.last_name` | body | `string` | no | — |
| `billing.company` | body | `string` | no | — |
| `billing.address_1` | body | `string` | no | — |
| `shipping.phone` | body | `string` | no | — |
| `billing.address_2` | body | `string` | no | — |
| `billing.city` | body | `string` | no | — |
| `billing.state` | body | `string` | no | — |
| `billing.postcode` | body | `string` | no | — |
| `meta_data[]` | body | `array` | no | — |
| `billing.country` | body | `string` | no | — |
| `billing.email` | body | `string` | no | — |
| `billing.phone` | body | `string` | no | — |
| `shipping` | body | `object` | no | — |
| `shipping.first_name` | body | `string` | no | — |
| `shipping.last_name` | body | `string` | no | — |
| `shipping.company` | body | `string` | no | — |
| `shipping.address_1` | body | `string` | no | — |
| `shipping.address_2` | body | `string` | no | — |
| `shipping.city` | body | `string` | no | — |
| `shipping.state` | body | `string` | no | — |
| `shipping.postcode` | body | `string` | no | — |
| `line_items[]` | body | `array<object>` | no | — |
| `shipping.country` | body | `string` | no | — |
| `line_items[].product_id` | body | `number` | no | — |
| `line_items[].variation_id` | body | `number` | no | — |
| `line_items[].quantity` | body | `number` | no | — |
| `line_items[].name` | body | `string` | no | — |
| `line_items[].tax_class` | body | `string` | no | — |
| `line_items[].subtotal` | body | `string` | no | — |
| `line_items[].total` | body | `string` | no | — |
| `shipping_lines[]` | body | `array<object>` | no | — |
| `shipping_lines[].method_id` | body | `string` | no | — |
| `shipping_lines[].method_title` | body | `string` | no | — |
| `currency` | body | `string` | no | — |
| `shipping_lines[].total` | body | `string` | no | — |
| `customer_note` | body | `string` | no | — |
| `fee_lines[]` | body | `array<object>` | no | — |
| `fee_lines[].name` | body | `string` | no | — |
| `fee_lines[].tax_class` | body | `string` | no | — |
| `fee_lines[].tax_status` | body | `string` | no | — |
| `coupon_lines[]` | body | `array<object>` | no | — |
| `fee_lines[].total` | body | `string` | no | — |
| `coupon_lines[].code` | body | `string` | no | — |
| `coupon_lines[].discount` | body | `string` | no | — |

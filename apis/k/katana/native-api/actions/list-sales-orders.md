# List Sales Orders with Katana

Lists sales orders in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales_orders`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Sales Orders](https://developer.katanamrp.com/reference/list-all-sales-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters sales orders by an array of IDs |
| `order_no` | query | `string` | no | Filters sales orders by an order number |
| `source` | query | `string` | no | Filters sales orders by a creation source |
| `location_id` | query | `number` | no | Filters sales orders by location |
| `customer_id` | query | `number` | no | Filters sales orders by customer |
| `status` | query | `string` | no | Filters sales orders by a status |
| `currency` | query | `string` | no | Filters sales orders by currency |
| `invoicing_status` | query | `string` | no | Filters sales orders by an invoicing status |
| `product_availability` | query | `string` | no | Filters sales orders by product availability |
| `ingredient_availability` | query | `string` | no | Filters sales orders by ingredient availability |
| `production_status` | query | `string` | no | Filters sales orders by production status |
| `ecommerce_order_type` | query | `string` | no | Filters sales orders by an e-commerce order type |
| `ecommerce_store_name` | query | `string` | no | Filters sales orders by an e-commerce store name |
| `ecommerce_order_id` | query | `string` | no | Filters sales orders by an e-commerce order id |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

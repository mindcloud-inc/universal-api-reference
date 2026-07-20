# List Manufacturing Orders with Katana

Lists manufacturing orders in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/manufacturing_orders`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Manufacturing Orders](https://developer.katanamrp.com/reference/getallmanufacturingorders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters manufacturing orders by an array of IDs |
| `status` | query | `string` | no | Filters manufacturing orders by a status. |
| `order_no` | query | `string` | no | Filters manufacturing orders by an order number. |
| `location_id` | query | `number` | no | Filters manufacturing orders by location. |
| `is_linked_to_sales_order` | query | `boolean` | no | Filters based on whether a manufacturing order is linked to a sales order or not. |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

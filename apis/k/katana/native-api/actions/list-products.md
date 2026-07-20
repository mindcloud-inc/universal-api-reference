# List Products with Katana

Lists products in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Products](https://developer.katanamrp.com/reference/list-all-products)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters products by an array of IDs |
| `name` | query | `string` | no | Filters products by a name |
| `uom` | query | `string` | no | Filters products by a uom |
| `is_sellable` | query | `boolean` | no | Filters products by a is_sellable |
| `is_producible` | query | `boolean` | no | Filters products by an is_producible |
| `is_purchasable` | query | `boolean` | no | Filters products by an is_purchasable |
| `is_auto_assembly` | query | `boolean` | no | Filters products by an is_auto_assembly |
| `default_supplier_id` | query | `number` | no | Filters products by a default_supplier_id |
| `batch_tracked` | query | `boolean` | no | Filters products by a batch_tracked |
| `serial_tracked` | query | `boolean` | no | Filters products by a serial_tracked |
| `operations_in_sequence` | query | `boolean` | no | Filters products by a operations_in_sequence |
| `purchase_uom` | query | `string` | no | Filters products by a purchase_uom |
| `purchase_uom_conversion_rate` | query | `number` | no | Filters products by a purchase_uom_conversion_rate |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `include_archived` | query | `boolean` | no | Archived data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

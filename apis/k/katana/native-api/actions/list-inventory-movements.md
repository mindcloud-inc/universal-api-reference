# List Inventory Movements with Katana

Lists inventory movements in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory_movements`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Inventory Movements](https://developer.katanamrp.com/reference/list-all-inventory-movements)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters inventory movements by an array of IDs |
| `variant_ids[]` | query | `array<number>` | no | Filters inventory movements by an array of variant ids |
| `location_id` | query | `number` | no | Filters inventory movements by a location_id |
| `resource_type` | query | `string` | no | Filters inventory movements by a resource type |
| `resource_id` | query | `number` | no | Filters inventory movements by a resource_id |
| `caused_by_order_no` | query | `string` | no | Filters inventory movements by a caused_by_order_no |
| `caused_by_resource_id` | query | `number` | no | Filters inventory movements by a caused_by_resource_id |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

# List Locations with Katana

Lists locations in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Locations](https://developer.katanamrp.com/reference/list-all-locations)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters locations by an array of IDs |
| `name` | query | `string` | no | Filters locations by a name |
| `legal_name` | query | `string` | no | Filters locations by a legal_name |
| `address_id` | query | `number` | no | Filters locations by an address_id |
| `sales_allowed` | query | `boolean` | no | Filters locations by a sales_allowed |
| `manufacturing_allowed` | query | `boolean` | no | Filters locations by a manufacturing_allowed |
| `purchases_allowed` | query | `boolean` | no | Filters locations by a purchases_allowed |
| `rank` | query | `number` | no | Filters locations by a rank |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

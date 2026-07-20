# List Suppliers with Katana

Lists suppliers in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/suppliers`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Suppliers](https://developer.katanamrp.com/reference/list-all-suppliers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filters suppliers by name |
| `ids[]` | query | `array<number>` | no | Filters suppliers by an array of IDs |
| `email` | query | `string` | no | Filters suppliers by an email |
| `phone` | query | `string` | no | Filters suppliers by a phone number |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

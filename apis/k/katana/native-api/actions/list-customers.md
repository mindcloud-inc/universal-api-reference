# List Customers with Katana

Lists customers in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Customers](https://developer.katanamrp.com/reference/list-all-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filters customers by name |
| `first_name` | query | `string` | no | Filters customers by first name |
| `last_name` | query | `string` | no | Filters customers by last name |
| `company` | query | `string` | no | Filters customers by company |
| `ids[]` | query | `array<number>` | no | Filters customers by an array of IDs |
| `email` | query | `string` | no | Filters customers by an email |
| `phone` | query | `string` | no | Filters customers by a phone number |
| `currency` | query | `string` | no | Filters customers by currency |
| `reference_id` | query | `string` | no | Filters customers by a reference ID |
| `category` | query | `string` | no | Filters customers by a category |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

# List Stores with Loyverse

Retrieves store records from the Loyverse account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stores`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Stores](https://developer.loyverse.com/docs/#tag/Stores)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_ids` | query | `string` | no | Return only store specified by a comma-separated list of IDs |
| `created_at_min` | query | `date` | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `created_at_max` | query | `date` | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_min` | query | `string` | no | Show resources updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_max` | query | `string` | no | Show resources updated before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `show_deleted` | query | `boolean` | no | Show deleted modifiers and modifier options |

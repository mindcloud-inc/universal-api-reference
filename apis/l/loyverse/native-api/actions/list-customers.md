# List Customers with Loyverse

Retrieves customer records from the Loyverse database.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Customers](https://developer.loyverse.com/docs/#tag/Customers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_ids` | query | `string` | no | Return only customers specified by a comma-separated list of IDs |
| `email` | query | `string` | no | Filter customers by email |
| `created_at_min` | query | `date` | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `created_at_max` | query | `date` | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_min` | query | `string` | no | Show resources updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_max` | query | `string` | no | Show resources updated before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |

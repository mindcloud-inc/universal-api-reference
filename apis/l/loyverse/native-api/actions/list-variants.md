# List Variants with Loyverse

Retrieves product variant records from Loyverse.

## Endpoint

- **Method:** `GET`
- **Path:** `/variants`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Variants](https://developer.loyverse.com/docs/#tag/Items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variants_ids` | query | `string` | no | Return only variants specified by a comma-separated list of IDs |
| `items_ids` | query | `string` | no | Return only variants attached to specified item ids |
| `sku` | query | `string` | no | Filter variants by sku |
| `created_at_min` | query | `date` | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `created_at_max` | query | `date` | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_min` | query | `string` | no | Show resources updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updated_at_max` | query | `string` | no | Show resources updated before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |
| `show_deleted` | query | `boolean` | no | Show deleted modifiers and modifier options |

# List Inventory Levels with Loyverse

Retrieves current inventory levels from Loyverse.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Inventory Levels](https://developer.loyverse.com/docs/#tag/Inventory)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_ids` | query | `string` | no | Show inventory levels only for specified stores |
| `variant_ids` | query | `string` | no | Show inventory levels only for specified variants |
| `updated_at_min` | query | `date` | no | Show inventory levels updated at or after specified date |
| `updated_at_max` | query | `date` | no | Show inventory levels updated at or before specified date |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |

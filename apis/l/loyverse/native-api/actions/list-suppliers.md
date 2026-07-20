# List Suppliers with Loyverse

Retrieves supplier records from the Loyverse account.

## Endpoint

- **Method:** `GET`
- **Path:** `/suppliers/`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [List Suppliers](https://developer.loyverse.com/docs/#tag/Suppliers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suppliers_ids` | query | `string` | no | Return only suppliers specified by a comma-separated list of IDs |
| `limit` | query | `number` | no | Used for pagination |
| `cursor` | query | `string` | no | Used for pagination |
| `show_deleted` | query | `boolean` | no | Show deleted modifiers and modifier options |

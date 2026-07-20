# Filter Inventory with Alto

Finds inventory items in Alto by filter criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/filter`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Filter Inventory](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryType` | query | `string` | no | Inventory category type filter. |
| `inventory-status` | query | `string` | no | Inventory status filter. |
| `recordType` | query | `string` | no | Inventory record type filter. |
| `branchIds` | query | `string` | no | One or more Alto branch IDs to filter inventory results. Send multiple values as a string separated by `,`. |

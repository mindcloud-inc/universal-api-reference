# List Inventory Lots with Fiddle

Retrieves inventory lot records from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory-lots`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Inventory Lots](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryItemId` | query | `string` | no | Inventory item ID filter |
| `status` | query | `string` | no | Status filter |

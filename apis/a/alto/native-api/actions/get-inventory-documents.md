# Get Inventory Documents with Alto

Retrieves documents for an inventory item in Alto.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/:inventoryId/documents`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Inventory Documents](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryId` | path | `string` | yes | Unique Alto inventory item identifier. |

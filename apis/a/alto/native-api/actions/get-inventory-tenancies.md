# Get Inventory Tenancies with Alto

Retrieves tenancies for an inventory item in Alto.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/:inventoryId/tenancies`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Inventory Tenancies](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryId` | path | `string` | yes | Unique Alto inventory item identifier. |

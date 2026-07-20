# Get Property Meter with InventoryBase

Retrieves a property meter from InventoryBase by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/properties/:propertyId/meters/:meterId`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Get Property Meter](https://developer.inventorybase.com/#get-a-single-meter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meterId` | path | `number` | yes | The ID of the meter |
| `propertyId` | path | `number` | yes | The ID of the property |

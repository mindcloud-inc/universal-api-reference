# Create Inspection with InventoryBase

Creates a new inspection in InventoryBase.

## Endpoint

- **Method:** `POST`
- **Path:** `/inspections`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Create Inspection](https://developer.inventorybase.com/#create-an-inspection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property` | body | `object` | yes | Property object containing the property ID |
| `type` | body | `object` | yes | Inspection type object containing the type ID |

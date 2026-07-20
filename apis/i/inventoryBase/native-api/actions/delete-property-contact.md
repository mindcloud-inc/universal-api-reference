# Delete Property Contact with InventoryBase

Deletes an existing property contact from InventoryBase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/properties/:propertyId/contacts/:contactId`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Delete Property Contact](https://developer.inventorybase.com/#delete-a-property-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | path | `number` | yes | The InventoryBase property ID. |
| `contactId` | path | `number` | yes | The InventoryBase contact ID. |

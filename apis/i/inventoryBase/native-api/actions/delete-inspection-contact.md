# Delete Inspection Contact with InventoryBase

Deletes an existing inspection contact from InventoryBase.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inspections/:inspectionId/contacts/:contactId`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Delete Inspection Contact](https://developer.inventorybase.com/#delete-an-inspection-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The ID of the contact |
| `inspectionId` | path | `number` | yes | The ID of the inspection |

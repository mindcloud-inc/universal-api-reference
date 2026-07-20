# Update Inspection Contact with InventoryBase

Updates an existing inspection contact in InventoryBase.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inspections/:inspectionId/contacts/:contactId`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Update Inspection Contact](https://developer.inventorybase.com/#update-an-inspection-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The ID of the contact |
| `deliver` | body | `boolean` | yes | Whether to deliver to the contact |
| `email` | body | `string` | yes | Contact email |
| `inspectionId` | path | `number` | yes | The ID of the inspection |
| `name` | body | `string` | yes | Contact name |
| `notify` | body | `boolean` | yes | Whether to notify the contact |
| `phone` | body | `string` | yes | Contact phone |
| `signee` | body | `boolean` | yes | Whether the contact is a signee |
| `type` | body | `number` | yes | Contact type ID |

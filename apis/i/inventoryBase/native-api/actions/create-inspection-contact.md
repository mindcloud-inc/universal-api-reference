# Create Inspection Contact with InventoryBase

Creates a new contact for an inspection in InventoryBase.

## Endpoint

- **Method:** `POST`
- **Path:** `/inspections/:inspectionId/contacts`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Create Inspection Contact](https://developer.inventorybase.com/#create-an-inspection-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliver` | body | `boolean` | yes | Whether to deliver to the contact |
| `email` | body | `string` | yes | Contact email |
| `inspectionId` | path | `number` | yes | The ID of the inspection |
| `name` | body | `string` | yes | Contact name |
| `notify` | body | `boolean` | yes | Whether to notify the contact |
| `phone` | body | `string` | yes | Contact phone |
| `signee` | body | `boolean` | yes | Whether the contact is a signee |
| `type` | body | `number` | yes | Contact type ID |

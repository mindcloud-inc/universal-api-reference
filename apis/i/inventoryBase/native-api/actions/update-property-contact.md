# Update Property Contact with InventoryBase

Updates an existing property contact in InventoryBase.

## Endpoint

- **Method:** `PUT`
- **Path:** `/properties/:propertyId/contacts/:contactId`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Update Property Contact](https://developer.inventorybase.com/#update-a-property-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliver` | body | `boolean` | yes | Whether to deliver to the contact |
| `email` | body | `string` | yes | Contact email |
| `name` | body | `string` | yes | Contact name |
| `notify` | body | `boolean` | yes | Whether to notify the contact |
| `phone` | body | `string` | yes | Contact phone |
| `propertyId` | path | `number` | yes | The InventoryBase property ID. |
| `signee` | body | `boolean` | yes | Whether the contact is a signee |
| `type` | body | `number` | yes | Contact type ID |
| `contactId` | path | `number` | yes | The InventoryBase contact ID. |

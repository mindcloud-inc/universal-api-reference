# Create Property Contact with InventoryBase

Creates a new contact for a property in InventoryBase.

## Endpoint

- **Method:** `POST`
- **Path:** `/properties/:propertyId/contacts`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Create Property Contact](https://developer.inventorybase.com/#create-a-property-contact)

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

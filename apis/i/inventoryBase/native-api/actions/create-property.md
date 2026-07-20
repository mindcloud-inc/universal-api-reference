# Create Property with InventoryBase

Creates a new property record in InventoryBase.

## Endpoint

- **Method:** `POST`
- **Path:** `/properties`
- **Base URL:** `https://api.inventorybase.com`
- **Official documentation:** [Create Property](https://developer.inventorybase.com/#creating-a-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `object` | yes | The property's address object. |
| `no_of_beds` | body | `number` | yes | The number of bedrooms. |
| `no_of_baths` | body | `number` | yes | The number of bathrooms. |
| `no_of_garages` | body | `number` | no | The number of garages. |
| `parking` | body | `boolean` | no | Whether the property has parking. |
| `garden` | body | `boolean` | no | Whether the property has a garden. |
| `furnished` | body | `string` | no | The furnished status. |
| `type` | body | `string` | no | The property type. |
| `ref` | body | `string` | no | A user-defined property reference. |
| `notes` | body | `string` | no | Notes about the property. |

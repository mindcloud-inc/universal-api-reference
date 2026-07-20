# Create Item with BoxHero

Creates a new item in BoxHero.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/items`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Create Item](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_createBarcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attrs` | body | `object` | no | Attributes of the item |
| `barcode` | body | `string` | no | Barcode used when scanning the item |
| `cost` | body | `string` | no | Purchase cost of the item |
| `location_id` | query | `number` | no | Location to use when creating the item |
| `name` | body | `string` | yes | The name of the item |
| `photo_url` | body | `string` | no | Photo URL for the item |
| `price` | body | `string` | no | Sale price of the item |
| `quantity` | body | `number` | no | Initial quantity of the item |
| `sku` | body | `string` | no | The SKU of the item |

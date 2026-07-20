# Update Item with BoxHero

Updates an existing item in BoxHero.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/items/:item_id`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [Update Item](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_editBarcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attrs` | body | `object` | no | Attributes of the item |
| `barcode` | body | `string` | no | Barcode used when scanning the item |
| `cost` | body | `string` | no | Purchase cost of the item |
| `item_id` | path | `number` | yes | Unique identifier for the item |
| `name` | body | `string` | no | The name of the item |
| `photo_url` | body | `string` | no | Photo URL for the item |
| `price` | body | `string` | no | Sale price of the item |
| `sku` | body | `string` | no | The SKU of the item |

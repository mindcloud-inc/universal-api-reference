# Get Inventory Item with Stockpilot

Retrieves an inventory item from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/get`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Get Inventory Item](https://api.stockpilot.dev/redoc#operation/get_inventory_item_inventory_get_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | Inventory item ID |
| `sku` | query | `string` | no | Inventory SKU |
| `barcode` | query | `string` | no | Inventory barcode |

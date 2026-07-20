# Create Inventory Item with Stockpilot

Creates a new inventory item in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory/create`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Create Inventory Item](https://api.stockpilot.dev/redoc#operation/create_inventory_inventory_create_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | body | `number` | yes | Product database ID |
| `sku` | body | `string` | yes | Stock keeping unit |
| `item_name` | body | `string` | yes | Inventory item name |
| `barcode` | body | `string` | yes | Item barcode |
| `barcode_type` | body | `string` | no | Barcode type |
| `quantity` | body | `number` | no | Available quantity |
| `moq` | body | `number` | no | Minimum order quantity |
| `stock_threshold` | body | `number` | no | Minimum stock threshold |
| `purchase_price` | body | `number` | no | Purchase price |
| `wholesale_price` | body | `number` | no | Wholesale price |
| `base_price` | body | `number` | no | Base price |
| `weight` | body | `string` | no | Weight value |
| `length` | body | `number` | no | Item length |
| `width` | body | `number` | no | Item width |
| `height` | body | `number` | no | Item height |
| `condition` | body | `string` | no | Item condition |
| `vat_class` | body | `string` | no | VAT class |
| `is_active` | body | `boolean` | no | Whether the item is active |

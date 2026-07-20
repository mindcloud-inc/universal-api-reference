# Update Inventory Item with Stockpilot

Updates an existing inventory item in Stockpilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory/update`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [Update Inventory Item](https://api.stockpilot.dev/redoc#operation/update_inventory_inventory_update_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | Internal Stockpilot product ID |
| `item_name` | body | `string` | no | Name of the item |
| `sku` | body | `string` | no | Stock Keeping Unit |
| `barcode` | body | `string` | no | Product barcode (EAN) |
| `quantity` | body | `number` | no | Stock quantity |
| `base_price` | body | `number` | no | Base price |
| `retail_price` | body | `number` | no | Retail price |
| `purchase_price` | body | `number` | no | Purchase price |
| `wholesale_price` | body | `number` | no | Wholesale price |
| `sale_price` | body | `number` | no | Sale price |
| `weight` | body | `string` | no | Weight as string |
| `length` | body | `number` | no | Length |
| `width` | body | `number` | no | Width |
| `height` | body | `number` | no | Height |
| `vat_class` | body | `string` | no | VAT class name |
| `condition` | body | `string` | no | Condition |
| `stock_threshold` | body | `number` | no | Minimum stock threshold for alerts |
| `moq` | body | `number` | no | Minimum order quantity |
| `assign_bin_location` | body | `string` | no | Assign bin location |
| `remove_bin_location` | body | `string` | no | Remove bin location |
| `threshold` | body | `string` | no | Threshold using format like 5u or 33w |
| `is_active` | body | `boolean` | no | Is the product active |

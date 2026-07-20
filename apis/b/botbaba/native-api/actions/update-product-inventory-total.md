# Update Product Inventory Total with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/EditProductInventoryTotal`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Update Product Inventory Total](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | body | `number` | yes | Bot identifier. |
| `inventoryDetails[]` | body | `array<object>` | yes | Inventory detail rows. |
| `inventoryDetails[].sku` | body | `string` | yes | Product SKU. |
| `inventoryDetails[].InventoryQty` | body | `number` | yes | Inventory quantity. |

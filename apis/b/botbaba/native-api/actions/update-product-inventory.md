# Update Product Inventory with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/EditProductInventory`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Update Product Inventory](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | body | `number` | yes | Bot identifier. |
| `inventoryDetails[]` | body | `array<object>` | yes | Inventory detail rows. |
| `inventoryDetails[].sku` | body | `string` | yes | Product SKU. |
| `inventoryDetails[].qty` | body | `number` | yes | Inventory quantity delta. |
| `inventoryDetails[].type` | body | `string` | yes | Inventory adjustment type. |

# Update Inventory Levels with Megaventory

Updates inventory levels in Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/InventoryLocationStockProductStockUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Inventory Levels](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationStockProductStockUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvProductStockUpdateList` | body | `list<object>` | yes | JSON array of inventory level update objects. |

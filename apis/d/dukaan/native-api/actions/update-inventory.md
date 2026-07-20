# Update Inventory with Dukaan

Updates inventory quantities in Dukaan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/store/seller/seller-warehouse-inventory/:inventoryItemUuid/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Update Inventory](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventoryItemUuid` | path | `string` | yes | Inventory item UUID from Dukaan inventory data. |
| `inventory_list[]` | body | `array<object>` | yes | Warehouse inventory quantity updates. |

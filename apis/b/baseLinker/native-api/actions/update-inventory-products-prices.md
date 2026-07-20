# Update Inventory Products Prices with BaseLinker

Updates inventory product prices in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Update Inventory Products Prices](https://api.baselinker.com/index.php?method=updateInventoryProductsPrices)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventory_id` | body | `number` | yes |
| `products` | body | `object` | yes |
| `parameters` | body | `object` | no |

# Get Inventory Products Prices with BaseLinker

Retrieves inventory product prices from BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Inventory Products Prices](https://api.baselinker.com/index.php?method=getInventoryProductsPrices)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventory_id` | body | `number` | yes |
| `page` | body | `number` | no |

# Update Inventory Products Stock with BaseLinker

Updates inventory product stock in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Update Inventory Products Stock](https://api.baselinker.com/index.php?method=updateInventoryProductsStock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventory_id` | body | `number` | yes | Inventory identifier. |
| `products` | body | `object` | yes | Stock update payload keyed by product and warehouse identifiers. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

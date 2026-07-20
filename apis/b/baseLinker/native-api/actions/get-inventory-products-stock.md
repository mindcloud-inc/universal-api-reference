# Get Inventory Products Stock with BaseLinker

Retrieves inventory product stock from BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Inventory Products Stock](https://api.baselinker.com/index.php?method=getInventoryProductsStock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventory_id` | body | `number` | yes | Inventory identifier. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

# Get Inventory Products Data with BaseLinker

Retrieves inventory product details from BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Inventory Products Data](https://api.baselinker.com/index.php?method=getInventoryProductsData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventory_id` | body | `number` | yes | Inventory identifier. |
| `products[]` | body | `array<number>` | yes | Array of product identifiers to fetch. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

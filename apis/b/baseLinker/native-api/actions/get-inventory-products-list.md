# Get Inventory Products List with BaseLinker

Retrieves basic inventory product data from BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Inventory Products List](https://api.baselinker.com/index.php?method=getInventoryProductsList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inventory_id` | body | `number` | yes | Inventory identifier. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

# Update Cell Value with QuintaDB

Updates a single cell value in QuintaDB.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/cell_values/:dtype_id/update_cell_value/:property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Update Cell Value](https://quintadb.com/api/index#update_cell)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dtype_id` | path | `string` | yes |
| `property_id` | path | `string` | yes |
| `val` | body | `string` | yes |

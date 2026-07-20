# Update Record with QuintaDB

Updates an existing record in QuintaDB.

## Endpoint

- **Method:** `PUT`
- **Path:** `/apps/:app_id/dtypes/:dtype_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Update Record](https://quintadb.com/api/index#update_record)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `dtype_id` | path | `string` | yes |
| `json_values` | body | `string` | yes |

# Delete Many Records with QuintaDB

Deletes multiple selected records from QuintaDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:app_id/dtypes/delete_multiple.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Delete Many Records](https://quintadb.com/api/index#delete_multiple)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | body | `string` | yes |
| `json_dtype_ids` | body | `string` | yes |

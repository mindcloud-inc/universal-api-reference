# Remove File with QuintaDB

Removes a file from a QuintaDB record.

## Endpoint

- **Method:** `GET`
- **Path:** `/dtypes/delete_dtype_file/:app_id/:dtype_id/:property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Remove File](https://quintadb.com/api/index#remove_files)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `dtype_id` | path | `string` | yes |
| `property_id` | path | `string` | yes |
| `single_file_name` | query | `string` | yes |

# Update All Records with QuintaDB

Updates all records in a QuintaDB form.

## Endpoint

- **Method:** `POST`
- **Path:** `/dtypes/confirm_action/:app_id/:entity_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Update All Records](https://quintadb.com/api/index#update_multiple_all_records)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `confirm_action` | body | `string` | yes |
| `entity_id` | path | `string` | yes |
| `update_id` | body | `string` | yes |
| `update_term` | body | `string` | yes |
| `view` | body | `string` | no |

# Delete Field with QuintaDB

Deletes an existing field from QuintaDB.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:app_id/entities/:entity_id/properties/:property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Delete Field](https://quintadb.com/api/index#delete_field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |
| `property_id` | path | `string` | yes |

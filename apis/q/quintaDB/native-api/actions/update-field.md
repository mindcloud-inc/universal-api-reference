# Update Field with QuintaDB

Updates an existing field in QuintaDB.

## Endpoint

- **Method:** `PUT`
- **Path:** `/apps/:app_id/entities/:entity_id/properties/:property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Update Field](https://quintadb.com/api/index#update_field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `property_id` | path | `string` | yes |

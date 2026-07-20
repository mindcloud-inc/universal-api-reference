# Get Field with QuintaDB

Retrieves a field from QuintaDB by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_id/entities/:entity_id/properties/:property_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Get Field](https://quintadb.com/api/index#get_field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |
| `property_id` | path | `string` | yes |

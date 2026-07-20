# List Fields with QuintaDB

Retrieves all fields from a QuintaDB form.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_id/entities/:entity_id/properties.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [List Fields](https://quintadb.com/api/index#get_fields)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |

# Create Field with QuintaDB

Creates a new field in QuintaDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:app_id/entities/:entity_id/properties.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Create Field](https://quintadb.com/api/index#create_field)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `type_name` | body | `string` | yes |

# Update Form with QuintaDB

Updates an existing form in QuintaDB.

## Endpoint

- **Method:** `PUT`
- **Path:** `/apps/:app_id/entities/:entity_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Update Form](https://quintadb.com/api/index#update_form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |
| `name` | body | `string` | yes |

# List Reports with QuintaDB

Retrieves reports from a QuintaDB form.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_id/entities/:entity_id/views/index.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [List Reports](https://quintadb.com/api/index#get_reports)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | path | `string` | yes |

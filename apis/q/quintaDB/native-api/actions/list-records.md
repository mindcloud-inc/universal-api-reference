# List Records with QuintaDB

Retrieves records from a QuintaDB form.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:app_id/dtypes/entity/:entity_id.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [List Records](https://quintadb.com/api/index#get_records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | — |
| `entity_id` | path | `string` | yes | Identifier of the QuintaDB form whose records should be listed. |
| `name_value` | query | `string` | no | — |
| `view` | query | `string` | no | — |

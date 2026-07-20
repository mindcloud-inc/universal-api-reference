# Create Record with QuintaDB

Creates a new record in QuintaDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:app_id/dtypes.json`
- **Base URL:** `https://quintadb.com`
- **Official documentation:** [Create Record](https://quintadb.com/api/index#create_record)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `app_id` | path | `string` | yes |
| `entity_id` | body | `string` | yes |
| `id` | body | `string` | no |
| `json_values` | body | `string` | no |

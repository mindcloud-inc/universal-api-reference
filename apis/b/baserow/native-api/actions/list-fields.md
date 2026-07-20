# List Fields with Baserow

Retrieves fields from a Baserow table.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/database/fields/table/:table_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [List Fields](https://api.baserow.io/api/redoc/#operation/list_database_table_fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table whose fields you want to inspect. |

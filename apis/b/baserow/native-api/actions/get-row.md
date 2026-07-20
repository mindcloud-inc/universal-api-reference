# Get Row with Baserow

Retrieves a row from Baserow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/database/rows/table/:table_id/:row_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [Get Row](https://api.baserow.io/api/redoc/#operation/get_database_table_row)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table containing the row. |
| `row_id` | path | `number` | yes | The row to fetch. |
| `user_field_names` | query | `boolean` | no | Use user-facing field names in the response. |
| `include` | query | `string` | no | Optional response metadata to include. |
| `view` | query | `number` | no | Optional view context for permissions and default values. |

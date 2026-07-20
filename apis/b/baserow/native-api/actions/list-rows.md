# List Rows with Baserow

Retrieves rows from a Baserow table.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/database/rows/table/:table_id/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [List Rows](https://api.baserow.io/api/redoc/#operation/list_database_table_rows)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `number` | yes | The Baserow table to read rows from. |
| `search` | query | `string` | no | Return only rows whose data matches this search query. |
| `search_mode` | query | `string` | no | Choose how Baserow should match the search term. |
| `include` | query | `string` | no | Comma-separated field names to include in the response. |
| `exclude` | query | `string` | no | Comma-separated field names to exclude from the response. |
| `user_field_names` | query | `boolean` | no | Return field names instead of field IDs in the row payload. |
| `filters` | query | `string` | no | JSON serialized filter tree for advanced row filtering. |

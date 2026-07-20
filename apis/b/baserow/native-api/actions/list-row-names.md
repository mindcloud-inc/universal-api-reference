# List Row Names with Baserow

Retrieves primary row names from Baserow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/database/rows/names/`
- **Base URL:** `https://api.baserow.io`
- **Official documentation:** [List Row Names](https://api.baserow.io/api/redoc/#operation/list_database_table_row_names)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | query | `number` | yes | The table whose row names you want to fetch. |
| `rowIds[]` | query | `array<number>` | yes | The row IDs whose primary-field names you want to fetch. |

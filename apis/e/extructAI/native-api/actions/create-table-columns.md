# Create Table Columns with Extruct AI

Creates table columns in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tables/:table_id/columns`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Create Table Columns](https://docs.extruct.ai/api-reference/tables/create-table-columns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `column_configs[]` | body | `array<object>` | yes | List of new column config objects. |
| `insert_after` | body | `string` | no | Defaults to true; may also be false or a column ID string. |

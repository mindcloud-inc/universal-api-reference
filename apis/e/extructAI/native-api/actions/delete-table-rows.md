# Delete Table Rows with Extruct AI

Deletes table rows from Extruct AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/tables/:table_id/rows`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Delete Table Rows](https://docs.extruct.ai/api-reference/tables/delete-table-rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `rows[]` | body | `array<string>` | yes | Array of row IDs to delete. |

# Delete Table Column with Extruct AI

Deletes a table column from Extruct AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/tables/:table_id/columns/:column_id`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Delete Table Column](https://docs.extruct.ai/api-reference/tables/delete-table-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `column_id` | path | `string` | yes | Target column identifier. |

# Update Table Column with Extruct AI

Updates a table column in Extruct AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/tables/:table_id/columns/:column_id`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Update Table Column](https://docs.extruct.ai/api-reference/tables/update-table-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `column_id` | path | `string` | yes | Target column identifier. |
| `name` | body | `string` | yes | Column display name. |
| `key` | body | `string` | yes | Column key. |

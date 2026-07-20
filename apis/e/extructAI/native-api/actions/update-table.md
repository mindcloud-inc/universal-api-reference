# Update Table with Extruct AI

Updates a table in Extruct AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/tables/:table_id`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Update Table](https://docs.extruct.ai/api-reference/tables/update-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `name` | body | `string` | no | New table name to set, if provided. |
| `description` | body | `string` | no | New table description to set, if provided. |
| `tags[]` | body | `array<string>` | no | New table tags to set, if provided. |
| `columns_order[]` | body | `array<string>` | no | New order of column IDs, if provided. |

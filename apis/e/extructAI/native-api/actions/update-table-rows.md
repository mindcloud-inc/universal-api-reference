# Update Table Rows with Extruct AI

Updates table rows in Extruct AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/tables/:table_id/rows`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Update Table Rows](https://docs.extruct.ai/api-reference/tables/update-table-rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `rows[]` | body | `array<object>` | yes | Array of row update objects; each requires `data` and can include `id` for the target row. |
| `run` | body | `boolean` | no | Whether to run the table after updating rows. |

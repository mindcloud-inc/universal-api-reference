# Get Row Data with Extruct AI

Retrieves table row data from Extruct AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tables/:table_id/rows/:row_id`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Get Row Data](https://docs.extruct.ai/api-reference/tables/get-table-row)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `row_id` | path | `string` | yes | Target row identifier. |

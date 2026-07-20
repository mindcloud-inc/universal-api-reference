# Add Input Data with Extruct AI

Adds input data rows to a table in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tables/:table_id/rows`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Add Input Data](https://docs.extruct.ai/api-reference/tables/create-table-rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `rows[]` | body | `array<object>` | yes | Array of row objects; each row must include data. |
| `run` | body | `boolean` | no | Defaults to false; set true to trigger a run after insert. |

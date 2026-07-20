# Run Enrichment with Extruct AI

Runs enrichment on a table in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tables/:table_id/run`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Run Enrichment](https://docs.extruct.ai/api-reference/tables/run-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Target table identifier. |
| `mode` | body | `string` | no | Defaults to new. Allowed values: new, all, failed. Accepted values: `0`, `1`, `2`. |
| `rows[]` | body | `array<string>` | no | Optional row IDs to scope the run. |
| `columns[]` | body | `array<string>` | no | Optional column IDs to scope the run. |

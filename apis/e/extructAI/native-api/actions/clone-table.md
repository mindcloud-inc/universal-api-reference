# Clone Table with Extruct AI

Clones a table in Extruct AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tables/:table_id/clone`
- **Base URL:** `https://api.extruct.ai`
- **Official documentation:** [Clone Table](https://docs.extruct.ai/api-reference/tables/clone-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `table_id` | path | `string` | yes | Source table identifier. |
| `schema_only` | query | `boolean` | no | Defaults to false; set true to clone structure without data. |

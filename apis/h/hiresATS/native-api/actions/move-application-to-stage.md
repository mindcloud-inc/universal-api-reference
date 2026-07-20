# Move Application To Stage with 100Hires ATS

Moves an application to a stage in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:id/move`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Move Application To Stage](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to move. |
| `stage_id` | body | `number` | yes | Target workflow stage ID. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |

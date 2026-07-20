# Transfer Application To Another Job with 100Hires ATS

Transfers an application to another job in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/:id/transfer`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Transfer Application To Another Job](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Application ID to transfer. |
| `job_id` | body | `number` | yes | Destination job ID. |
| `stage_id` | body | `number` | no | Optional destination stage ID. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |

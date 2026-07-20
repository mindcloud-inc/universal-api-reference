# Update Job Status with 100Hires ATS

Updates a job's status in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:id/status`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Update Job Status](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Job ID or alias to update status for. |
| `status` | body | `string` | yes | New job status name. |
| `include` | query | `string` | no | Optional comma-separated related job resources to include. |

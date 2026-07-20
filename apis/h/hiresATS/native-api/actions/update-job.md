# Update Job with 100Hires ATS

Updates an existing job in 100Hires ATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/:id`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Update Job](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Job ID or alias to update. |
| `title` | body | `string` | no | Optional updated public job title. |
| `description` | body | `string` | no | Optional updated job description. |
| `status` | body | `string` | no | Optional updated job status. |
| `location_city` | body | `string` | no | Optional updated job location city. |
| `location_country` | body | `string` | no | Optional updated job location country. |
| `workflow_id` | body | `number` | no | Optional updated workflow ID. |
| `is_remote` | body | `boolean` | no | Optional remote flag. |
| `internal_title` | body | `string` | no | Optional updated internal title. |
| `internal_job_id` | body | `string` | no | Optional updated internal job identifier. |
| `include` | query | `string` | no | Optional comma-separated related job resources to include. |

# Create Job with 100Hires ATS

Creates a new job in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Create Job](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `number` | yes | Company ID that owns the job. |
| `status` | body | `string` | yes | Initial job status name. |
| `title` | body | `string` | yes | Public job title. |
| `description` | body | `string` | yes | Job description in HTML or text. |
| `location_city` | body | `string` | yes | Job location city. |
| `location_country` | body | `string` | yes | Job location country. |
| `workflow_id` | body | `number` | no | Optional workflow ID to apply to the job. |
| `is_remote` | body | `boolean` | no | Whether the job is remote. |
| `internal_title` | body | `string` | no | Optional internal-only job title. |
| `internal_job_id` | body | `string` | no | Optional internal identifier for the job. |
| `include` | query | `string` | no | Optional comma-separated related job resources to include. |

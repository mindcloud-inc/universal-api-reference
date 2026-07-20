# Update Candidate with 100Hires ATS

Updates an existing candidate in 100Hires ATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/candidates/:id`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Update Candidate](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Candidate ID or alias to update. |
| `first_name` | body | `string` | no | Optional updated first name. |
| `last_name` | body | `string` | no | Optional updated last name. |
| `email` | body | `string` | no | Optional updated email address. |
| `phone` | body | `string` | no | Optional updated phone number. |
| `job_id` | body | `number` | no | Optional updated job ID attachment. |
| `stage_id` | body | `number` | no | Optional updated stage ID attachment. |
| `profile` | body | `object` | no | Optional key-value map of updated profile answers. |
| `company_id` | body | `number` | no | Optional target company ID. |
| `include` | query | `string` | no | Optional include selector for related application summaries. |

# Create Candidate with 100Hires ATS

Creates a new candidate in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Create Candidate](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | Candidate first name. |
| `last_name` | body | `string` | no | Candidate last name. |
| `email` | body | `string` | no | Candidate email address. |
| `phone` | body | `string` | no | Candidate phone number. |
| `job_id` | body | `number` | no | Optional job ID to attach the candidate to on creation. |
| `stage_id` | body | `number` | no | Optional stage ID to place the candidate in on creation. |
| `profile` | body | `object` | no | Optional key-value map of profile answers. |
| `company_id` | body | `number` | no | Optional target company ID. |
| `include` | query | `string` | no | Optional include selector for related application summaries. |

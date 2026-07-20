# Create Application with 100Hires ATS

Creates a new application in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/applications`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Create Application](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | body | `string` | yes | Candidate ID or alias to attach to the application. |
| `job_id` | body | `number` | yes | Job ID that the candidate is applying to. |
| `stage_id` | body | `number` | no | Optional stage ID to place the application into immediately. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |

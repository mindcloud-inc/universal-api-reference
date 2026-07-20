# List Applications with 100Hires ATS

Lists the applications in 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [List Applications](https://100hires.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate_id` | query | `number` | no | Return only applications for this candidate ID. |
| `job_id` | query | `number` | no | Return only applications for this job ID. |
| `stage_id` | query | `number` | no | Return only applications in this stage ID. |
| `status` | query | `string` | no | Filter by application status: pending, hired, or rejected. |
| `created_after` | query | `date` | no | Return only applications created after this Unix timestamp. |
| `updated_after` | query | `date` | no | Return only applications updated after this Unix timestamp. |
| `ai_score_min` | query | `number` | no | Return only applications with AI score at or above this value. |
| `ai_score_max` | query | `number` | no | Return only applications with AI score at or below this value. |
| `sort` | query | `string` | no | Sort order: created_at, -created_at, ai_score, or -ai_score. |
| `include` | query | `string` | no | Comma-separated related application resources to include. |

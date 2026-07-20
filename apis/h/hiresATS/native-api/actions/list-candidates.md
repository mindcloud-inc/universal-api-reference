# List Candidates with 100Hires ATS

Lists the candidates in 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/candidates`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [List Candidates](https://100hires.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional search by candidate name or email. |
| `email` | query | `string` | no | Optional exact email filter. |
| `full_name` | query | `string` | no | Optional full-name filter. |
| `job_id` | query | `number` | no | Optional job ID to filter candidates by job. |
| `linkedin` | query | `string` | no | Optional LinkedIn URL or alias filter. |
| `company_id` | query | `number` | no | Optional target company ID. Defaults to the authenticated company. |
| `created_after` | query | `number` | no | Optional Unix timestamp (seconds) lower bound for created_at. |
| `updated_after` | query | `number` | no | Optional Unix timestamp (seconds) lower bound for updated_at. |
| `include` | query | `string` | no | Optional include selector for related application summaries. |

# List Jobs with 100Hires ATS

Lists the jobs in 100Hires ATS.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [List Jobs](https://100hires.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional partial search across job title or internal title. |
| `status` | query | `string` | no | Optional job status name to filter by. |
| `company_id` | query | `number` | no | Optional target company ID. Defaults to the authenticated company. |
| `department_id` | query | `number` | no | Optional department ID to filter jobs. |
| `created_at_start` | query | `number` | no | Optional Unix timestamp (seconds) lower bound for created_at. |
| `created_at_end` | query | `number` | no | Optional Unix timestamp (seconds) upper bound for created_at. |
| `updated_after` | query | `number` | no | Optional Unix timestamp (seconds) lower bound for updated_at. |
| `include` | query | `string` | no | Optional comma-separated related job resources to include. |

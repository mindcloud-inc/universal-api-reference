# List Assessments with Testfuse

Retrieves assessments from Testfuse by assessment spec.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/assessments/`
- **Base URL:** `https://gateway.testfuse.com`
- **Official documentation:** [List Assessments](https://api.testfuse.com)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assess_status` | query | `string` | no |
| `page` | query | `number` | no |
| `search` | query | `string` | no |
| `size` | query | `number` | no |
| `sort` | query | `string` | no |
| `sort_direction` | query | `string` | no |
| `spec_id` | query | `string` | yes |

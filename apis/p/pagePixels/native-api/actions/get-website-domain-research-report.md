# Get Website Domain Research Report with PagePixels

## Endpoint

- **Method:** `GET`
- **Path:** `/api/domain_research_requests/:job_id/report`
- **Base URL:** `https://api.pagepixels.com`
- **Official documentation:** [Get Website Domain Research Report](https://pagepixels.com/app/screenshots-api-documentation#domain-research-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The PagePixels domain research job ID. |
| `format` | query | `string` | no | Optional output format. Use csv for CSV output; omit for JSON. |

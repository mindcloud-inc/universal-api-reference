# List Jobs with SEOTakeoff

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/jobs`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [List Jobs](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | query | `string` | yes | Tenant slug or ID to scope the jobs list. Example: mindcloud-co. |
| `status` | query | `string` | no | Optional job status to filter by, such as queued, processing, completed, or failed. |

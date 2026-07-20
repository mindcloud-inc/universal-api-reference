# Create Job with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/job.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Create Job](https://developer.servicem8.com/reference/createjobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_uuid` | body | `string` | no | Existing client UUID to attach to the new job. |
| `status` | body | `string` | no | Initial ServiceM8 job status. |
| `job_address` | body | `string` | no | Address for the new job. |
| `job_description` | body | `string` | no | Description for the new job. |

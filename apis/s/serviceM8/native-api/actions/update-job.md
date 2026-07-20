# Update Job with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/job/:uuid.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Update Job](https://developer.servicem8.com/reference/updatejobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Record UUID of the job to update. |
| `status` | body | `string` | no | Updated ServiceM8 job status. |
| `job_address` | body | `string` | no | Updated job address. |
| `job_description` | body | `string` | no | Updated job description. |

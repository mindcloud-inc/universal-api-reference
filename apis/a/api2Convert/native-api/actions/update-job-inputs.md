# Update Job Inputs with Api2Convert

Updates input files for a job in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/jobs/:job_id/input`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Job Inputs](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job whose inputs should be updated. |
| `body` | body | `object` | yes | Patch payload for the job input collection. |

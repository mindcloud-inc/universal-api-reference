# Update Job Outputs with Api2Convert

Updates output files for a job in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/jobs/:job_id/output`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Job Outputs](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job whose output files should be updated. |
| `body` | body | `object` | yes | Patch payload applied to the job output collection. |

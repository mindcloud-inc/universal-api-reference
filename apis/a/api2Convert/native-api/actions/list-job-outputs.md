# List Job Outputs with Api2Convert

Retrieves output files for a job from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/output`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [List Job Outputs](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job whose output files should be listed. |
| `conversion_id` | query | `string` | no | Filter output files by conversion identifier. |
| `input_id` | query | `string` | no | Filter output files by input identifier. |

# Get Job Output with Api2Convert

Retrieves an output file from a job in Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/output/:file_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Job Output](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | ID of the job that owns the output file. |
| `file_id` | path | `string` | yes | ID of the output file. |

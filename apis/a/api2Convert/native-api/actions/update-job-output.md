# Update Job Output with Api2Convert

Updates an output file for a job in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/jobs/:job_id/output/:file_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Job Output](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the output file. |
| `file_id` | path | `string` | yes | Unique identifier of the output file to update. |
| `body` | body | `object` | yes | Patch payload applied to the output file. |

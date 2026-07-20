# Update Job Input with Api2Convert

Updates an input file for a job in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/jobs/:job_id/input/:file_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Job Input](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the input file. |
| `file_id` | path | `string` | yes | Unique identifier of the input file to update. |
| `body` | body | `object` | yes | Patch payload that updates credentials for the input file. |

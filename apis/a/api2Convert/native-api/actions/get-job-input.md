# Get Job Input with Api2Convert

Retrieves an input file from a job in Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/input/:file_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Job Input](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | ID of the job. |
| `file_id` | path | `string` | yes | ID of the file. |

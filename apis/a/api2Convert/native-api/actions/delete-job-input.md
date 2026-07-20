# Delete Job Input with Api2Convert

Deletes an input file from a job in Api2Convert.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/jobs/:job_id/input/:file_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Delete Job Input](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the input file. |
| `file_id` | path | `string` | yes | Unique identifier of the input file to delete. |

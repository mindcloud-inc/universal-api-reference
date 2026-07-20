# Delete Job Output with Api2Convert

Deletes an output file from a job in Api2Convert.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/jobs/:job_id/output/:file_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Delete Job Output](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the output file. |
| `file_id` | path | `string` | yes | Unique identifier of the output file to delete. |

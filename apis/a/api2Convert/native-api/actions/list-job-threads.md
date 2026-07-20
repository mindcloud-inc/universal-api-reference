# List Job Threads with Api2Convert

Retrieves processing threads for a job from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/threads`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [List Job Threads](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job whose threads should be listed. |

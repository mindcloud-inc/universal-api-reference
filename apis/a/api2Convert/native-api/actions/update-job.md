# Update Job with Api2Convert

Updates an existing job in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/jobs/:job_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Job](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job to update. |
| `body` | body | `object` | yes | Full job payload used to update the job. |

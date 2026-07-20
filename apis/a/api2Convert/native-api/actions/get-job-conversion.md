# Get Job Conversion with Api2Convert

Retrieves a job conversion from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:job_id/conversions/:conversion_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Job Conversion](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | ID of the job. |
| `conversion_id` | path | `string` | yes | ID of the conversion. |

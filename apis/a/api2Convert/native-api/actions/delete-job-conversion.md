# Delete Job Conversion with Api2Convert

Deletes a job conversion from Api2Convert.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/jobs/:job_id/conversions/:conversion_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Delete Job Conversion](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the conversion. |
| `conversion_id` | path | `string` | yes | Unique identifier of the conversion to delete. |

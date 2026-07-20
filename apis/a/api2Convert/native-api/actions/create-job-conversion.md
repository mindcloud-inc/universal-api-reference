# Create Job Conversion with Api2Convert

Creates a conversion for a job in Api2Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:job_id/conversions`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Create Job Conversion](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the conversion. |
| `body` | body | `object` | yes | Conversion payload for the job, including the target and options. |

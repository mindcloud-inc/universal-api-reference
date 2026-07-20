# Update Job Conversion with Api2Convert

Updates an existing job conversion in Api2Convert.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/jobs/:job_id/conversions/:conversion_id`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Update Job Conversion](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that owns the conversion. |
| `conversion_id` | path | `string` | yes | Unique identifier of the conversion to update. |
| `body` | body | `object` | yes | Patch payload for the conversion, including options and metadata. |

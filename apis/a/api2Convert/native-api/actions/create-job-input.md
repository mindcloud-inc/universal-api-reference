# Create Job Input with Api2Convert

Creates an input file for a job in Api2Convert.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:job_id/input`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Create Job Input](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Unique identifier of the job that will receive the input file. |
| `body` | body | `object` | yes | Input file payload describing the source file to attach to the job. |

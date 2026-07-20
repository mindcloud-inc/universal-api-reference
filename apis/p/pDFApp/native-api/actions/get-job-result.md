# Get Job Result with PDF-app

Retrieves an async job result from PDF-app.

## Endpoint

- **Method:** `GET`
- **Path:** `/async_jobid_check`
- **Base URL:** `https://api.pdf-app.net`
- **Official documentation:** [Get Job Result](https://pdf-app.net/apidocumentation?type=async_jobid_check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | body | `string` | yes | The asynchronous job ID to look up. |

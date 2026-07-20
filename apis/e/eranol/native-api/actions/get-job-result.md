# Get Job Result with Eranol

Retrieves the result of an Eranol job.

## Endpoint

- **Method:** `GET`
- **Path:** `/ffmpeg/result/:job_id`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Get Job Result](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Job ID returned by an Eranol create action. |

# Get Job Status with ActivityInfo

Retrieves a job's status from ActivityInfo.

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/jobs/:jobId`
- **Base URL:** `https://www.activityinfo.org`
- **Official documentation:** [Get Job Status](https://www.activityinfo.org/support/docs/api/reference/getJobStatus.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | ActivityInfo long-running job ID. |

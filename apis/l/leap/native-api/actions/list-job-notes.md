# List Job Notes with Leap

Retrieves notes for a job from Leap.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/[:jobId]/notes`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [List Job Notes](https://docs.api.jobprogress.com/api/job-note.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | Leap job ID. |

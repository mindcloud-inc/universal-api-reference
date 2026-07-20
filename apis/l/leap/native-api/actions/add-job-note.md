# Add Job Note with Leap

Creates a new note for a job in Leap.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/[:jobId]/notes`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [Add Job Note](https://docs.api.jobprogress.com/api/job-note.json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | Leap job ID. |
| `note` | body | `string` | yes | Text to add as the job note. |

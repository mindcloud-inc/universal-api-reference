# Update Job Note with Leap

Updates an existing job note in Leap.

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/notes/[:noteId]`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [Update Job Note](https://docs.api.jobprogress.com/api/job-note.json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note` | body | `string` | yes | Updated text for the job note. |
| `noteId` | path | `number` | yes | Leap job note ID. |

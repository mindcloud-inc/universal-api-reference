# Upload Resume with CATS

Uploads a resume for a candidate in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates/:id/resumes`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Upload Resume](https://docs.catsone.com/api/v3/#candidates-upload-a-resume)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the candidate that the resume is being attached to. |
| `filename` | query | `string` | yes | The name to save the file being uploaded as. |
| `file` | body | `file` | yes | The resume file content to upload. |

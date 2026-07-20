# Parse Resume CV with SharpAPI

Creates a resume parsing job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/parse_resume`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Parse Resume CV](https://sharpapi.com/en/catalog/ai/hr-tech/resume-cv-parsing)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Upload the resume or CV file to parse. |
| `language` | body | `string` | no | Language for the parsed output. |

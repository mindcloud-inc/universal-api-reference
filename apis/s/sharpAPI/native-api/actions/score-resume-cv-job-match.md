# Score Resume CV Job Match with SharpAPI

Creates a resume job match scoring job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/hr/resume_job_match_score`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Score Resume CV Job Match](https://sharpapi.com/en/catalog/ai/hr-tech/resume-cv-job-match-score)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Resume or CV file to score against the job description. |
| `content` | body | `string` | yes | Full job description used for the match score. |
| `language` | body | `string` | no | Language for the score explanation output. |
| `context` | body | `string` | no | Additional scoring instructions for the match engine. |

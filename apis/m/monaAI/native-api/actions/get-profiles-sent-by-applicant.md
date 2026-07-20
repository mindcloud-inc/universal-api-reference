# Get Profiles Sent By Applicant with Mona AI

Retrieves sent profiles for an applicant from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/matching/getProfilesSentByApplicantId`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Profiles Sent By Applicant](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | body | `string` | yes | Applicant identifier whose sent profiles should be returned. |

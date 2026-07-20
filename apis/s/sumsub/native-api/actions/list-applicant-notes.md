# List Applicant Notes with Sumsub

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/api/applicants/notes`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [List Applicant Notes](https://docs.sumsub.com/reference/get-applicant-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | query | `string` | yes | — |
| `offset` | query | `number` | no | Optional pagination offset. Sumsub defaults to 0. |
| `limit` | query | `number` | no | Optional pagination limit. Sumsub defaults to 100. |

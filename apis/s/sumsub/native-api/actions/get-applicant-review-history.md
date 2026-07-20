# Get Applicant Review History with Sumsub

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/applicants/:id/review/history`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Get Applicant Review History](https://docs.sumsub.com/reference/get-applicant-review-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `levelName` | query | `string` | no | Optional Sumsub level name to filter the review history response. |

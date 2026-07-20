# List Applicant Actions with Sumsub

## Endpoint

- **Method:** `GET`
- **Path:** `/resources/applicantActions/-;applicantId=:applicantId`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [List Applicant Actions](https://docs.sumsub.com/reference/get-applicant-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | path | `string` | yes | Existing Sumsub applicant identifier. |
| `limit` | query | `number` | no | Maximum number of applicant actions to return. |
| `offset` | query | `number` | no | Pagination offset. |

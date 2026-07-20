# Create Application with Recooty

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/jobs/{{jobId}}/application`
- **Base URL:** `https://standaloneapi.recooty.app/api`
- **Official documentation:** [Create Application](https://api.recooty.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The Recooty job ID. |
| `first_name` | body | `string` | yes | Applicant first name. |
| `last_name` | body | `string` | yes | Applicant last name. |
| `email` | body | `string` | yes | Applicant email address. |
| `mobile_number` | body | `string` | yes | Applicant mobile number. |
| `resume` | body | `string` | yes | Resume file input or file URL, depending on your runtime connector input. |

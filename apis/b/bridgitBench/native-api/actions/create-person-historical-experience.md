# Create Person Historical Experience with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Historical Experience](https://developers.gobridgit.com/reference/personhistoricalexperiences_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID. |
| `personId` | path | `number` | yes | The person ID. |
| `projectName` | body | `string` | yes | — |
| `projectStartDate` | body | `date` | no | — |
| `projectEndDate` | body | `date` | no | — |
| `roleName` | body | `string` | yes | — |
| `currentCompany` | body | `boolean` | yes | — |
| `experienceFields[]` | body | `array<object>` | yes | — |
| `experienceFields[].experienceFieldId` | body | `string` | yes | — |
| `experienceFields[].experienceFieldValueId` | body | `string` | no | — |
| `experienceFields[].value` | body | `string` | no | — |
| `projectDescription` | body | `string` | no | — |
| `companyName` | body | `string` | no | — |
| `assignmentStartDate` | body | `date` | no | — |
| `assignmentEndDate` | body | `date` | no | — |
| `assignmentDuration` | body | `number` | no | — |
| `assignmentHours` | body | `number` | no | — |

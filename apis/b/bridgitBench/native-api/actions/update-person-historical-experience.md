# Update Person Historical Experience with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Historical Experience](https://developers.gobridgit.com/reference/personhistoricalexperiences_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The Person ID |
| `historicalExperienceId` | path | `string` | yes | The Historical Experience ID |
| `roleName` | body | `string` | yes | — |
| `experienceFields[]` | body | `array<object>` | yes | — |
| `experienceFields[].experienceFieldId` | body | `string` | yes | — |
| `experienceFields[].experienceFieldValueId` | body | `string` | no | — |
| `experienceFields[].value` | body | `string` | no | — |
| `assignmentStartDate` | body | `date` | no | — |
| `assignmentEndDate` | body | `date` | no | — |
| `assignmentDuration` | body | `number` | no | — |
| `assignmentHours` | body | `number` | no | — |

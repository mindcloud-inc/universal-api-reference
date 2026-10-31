# Create Project with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Projects`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project](https://developers.gobridgit.com/reference/projects_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `name` | body | `string` | yes | — |
| `colour` | body | `string` | no | The color associated with the project, expressed as a web color string: a '#' character, followed by a six-digit hexadecimal number. If not provided, color rules will be evaluated. |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
| `startTime` | body | `string` | no | The daily start time for the project. When omitted, the account default is used, falling back to the rp-api default. |
| `endTime` | body | `string` | no | The daily end time for the project. When omitted, the account default is used, falling back to the rp-api default. |
| `workDays` | body | `list<number>` | no | The days of the week the project is active. When omitted, the account default is used, falling back to the rp-api default. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Send multiple values as a array. |
| `hoursPerWeek` | body | `number` | no | The number of hours per week a salaried person works, for forecasting and budgeting calculations. When omitted, the account default is used, falling back to the rp-api default. |
| `type` | body | `list<string>` | yes | Accepted values: `Awarded`, `Opportunity`. |
| `winPercent` | body | `number` | no | — |
| `fields[]` | body | `array<object>` | no | — |
| `fields[].fieldId` | body | `number` | yes | — |
| `fields[].values[]` | body | `array<string>` | yes | — |
| `groupings[]` | body | `array<number>` | no | — |
| `description` | body | `string` | no | — |
| `phases[]` | body | `array<object>` | no | — |
| `phases[].id` | body | `number` | yes | — |
| `phases[].startDate` | body | `date` | yes | — |
| `phases[].endDate` | body | `date` | yes | — |

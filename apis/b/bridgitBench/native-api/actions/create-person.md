# Create Person with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person](https://developers.gobridgit.com/reference/persons_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `email` | body | `string` | no | — |
| `uniqueId` | body | `string` | no | — |
| `name` | body | `string` | yes | Maximum length: 250. |
| `type` | body | `list<string>` | yes | Accepted values: `Hourly`, `Salaried`. |
| `title` | body | `string` | no | Maximum length: 250. |
| `photoUrl` | body | `string` | no | — |
| `employmentDates` | body | `object` | no | Request object for representing employment dates on a person. |
| `workDays` | body | `list<number>` | yes | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Send multiple values as a array. |
| `fields[]` | body | `array<object>` | no | — |
| `fields[].fieldId` | body | `number` | yes | — |
| `fields[].values[]` | body | `array<string>` | yes | — |
| `groupings[]` | body | `array<number>` | no | — |
| `industryStartDate` | body | `date` | no | — |
| `titleEffectiveDate` | body | `date` | no | — |

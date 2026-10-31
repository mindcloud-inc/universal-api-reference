# Create Person Historical Experience Field with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Historical Experience Field](https://developers.gobridgit.com/reference/personhistoricalexperiencefields_post)

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
| `historicalExperienceId` | path | `string` | yes | The historical experience ID. |
| `experienceFields[]` | body | `array<object>` | yes | — |
| `experienceFields[].experienceFieldId` | body | `string` | yes | — |
| `experienceFields[].experienceFieldValueId` | body | `string` | no | — |
| `experienceFields[].value` | body | `string` | no | — |

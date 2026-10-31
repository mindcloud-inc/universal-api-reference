# Update Person Historical Experience Field with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId/experience-fields/:experienceFieldId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Historical Experience Field](https://developers.gobridgit.com/reference/personhistoricalexperiencefields_patch)

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
| `experienceFieldId` | path | `string` | yes | The experience field ID. |
| `values[]` | body | `array<object>` | no | The full set of values to store for the field. Replaces whatever is currently stored: added values create rows, removed values delete their rows. Multiple values are only supported for multi-select fields; cannot be combined with experienceFieldValueId/value. |
| `values[].experienceFieldValueId` | body | `string` | no | — |
| `values[].value` | body | `string` | no | — |
| `experienceFieldValueId` | body | `string` | no | — |
| `value` | body | `string` | no | — |

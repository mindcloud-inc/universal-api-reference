# Set Person Field Values with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/person-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Set Person Field Values](https://developers.gobridgit.com/reference/personfieldvalue_setfieldvalues)

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
| `titleEffectiveDate` | query | `date` | no | — |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].fieldId` | body | `number` | yes | — |
| `payload[].values[]` | body | `array<string>` | yes | — |

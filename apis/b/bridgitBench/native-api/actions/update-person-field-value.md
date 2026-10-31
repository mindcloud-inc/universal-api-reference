# Update Person Field Value with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/person-field-values/:fieldId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Field Value](https://developers.gobridgit.com/reference/personfieldvalue_updatefieldvalue)

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
| `fieldId` | path | `number` | yes | The field ID |
| `titleEffectiveDate` | query | `date` | no | — |
| `values[]` | body | `array<string>` | yes | — |

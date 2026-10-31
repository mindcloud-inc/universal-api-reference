# Clear Person Field Values with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/person-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Clear Person Field Values](https://developers.gobridgit.com/reference/personfieldvalue_clearfieldvalues)

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
| `payload[]` | body | `array<number>` | yes | — |

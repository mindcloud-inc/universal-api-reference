# Update Project Field Values with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Field Values](https://developers.gobridgit.com/reference/projectfieldvalue_bulkupdatefieldvalues)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The Project ID |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].fieldId` | body | `number` | yes | — |
| `payload[].values[]` | body | `array<string>` | yes | — |

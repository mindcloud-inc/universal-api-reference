# Update Project Field Value with Bridgit Bench

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values/:fieldId`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Project Field Value](https://developers.gobridgit.com/reference/projectfieldvalue_updatefieldvalue)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the role belongs to |
| `fieldId` | path | `number` | yes | The field ID that the data can be updated |
| `values[]` | body | `array<string>` | yes | — |

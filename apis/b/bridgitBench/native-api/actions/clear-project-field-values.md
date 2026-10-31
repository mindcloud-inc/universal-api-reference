# Clear Project Field Values with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Clear Project Field Values](https://developers.gobridgit.com/reference/projectfieldvalue_clearfieldvalues)

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
| `payload[]` | body | `array<number>` | yes | — |

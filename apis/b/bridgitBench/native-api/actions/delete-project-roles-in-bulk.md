# Delete Project Roles in Bulk with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/bulk`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Project Roles in Bulk](https://developers.gobridgit.com/reference/projectroles_bulkremove)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID that the role belongs to |
| `payload[]` | body | `array<number>` | yes | — |

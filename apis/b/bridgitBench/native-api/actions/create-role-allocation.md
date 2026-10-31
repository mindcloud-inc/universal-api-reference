# Create Role Allocation with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/roles/:roleId/allocations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Role Allocation](https://developers.gobridgit.com/reference/roleallocations_post)

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
| `roleId` | path | `number` | yes | The Role ID |
| `personId` | body | `number` | yes | — |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |

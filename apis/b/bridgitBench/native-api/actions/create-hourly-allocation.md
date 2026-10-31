# Create Hourly Allocation with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/hourly-allocations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Hourly Allocation](https://developers.gobridgit.com/reference/hourlyallocations_post)

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
| `roleId` | body | `number` | yes | — |
| `personId` | body | `number` | yes | — |
| `startDate` | body | `date` | no | — |
| `endDate` | body | `date` | no | — |
| `roleStartDate` | body | `date` | no | Optional. When provided, updates the unfilled role's start date before creating the allocation. Must be set together with ResourcePlanning.Contracts.ProjectAllocationRequest.RoleEndDate — supplying only one will fail validation. |
| `roleEndDate` | body | `date` | no | Optional. When provided, updates the unfilled role's end date before creating the allocation. Must be set together with ResourcePlanning.Contracts.ProjectAllocationRequest.RoleStartDate — supplying only one will fail validation. |

# Create Project Task Role Allocations in Bulk with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/allocations/bulk`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Task Role Allocations in Bulk](https://developers.gobridgit.com/reference/projecttasks_bulkaddallocation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID |
| `taskId` | path | `string` | yes | The task ID |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].roleId` | body | `number` | yes | — |
| `payload[].personId` | body | `number` | yes | — |
| `payload[].startDate` | body | `date` | no | — |
| `payload[].endDate` | body | `date` | no | — |
| `payload[].roleStartDate` | body | `date` | no | Optional. When provided, updates the unfilled role's start date before creating the allocation. Must be set together with ResourcePlanning.Contracts.ProjectAllocationRequest.RoleEndDate — supplying only one will fail validation. |
| `payload[].roleEndDate` | body | `date` | no | Optional. When provided, updates the unfilled role's end date before creating the allocation. Must be set together with ResourcePlanning.Contracts.ProjectAllocationRequest.RoleStartDate — supplying only one will fail validation. |

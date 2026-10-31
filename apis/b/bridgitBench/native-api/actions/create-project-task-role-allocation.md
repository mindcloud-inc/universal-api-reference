# Create Project Task Role Allocation with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:taskId/roles/:id/allocations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Task Role Allocation](https://developers.gobridgit.com/reference/projecttasks_addallocation)

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
| `id` | path | `number` | yes | The role ID the task role belongs to |
| `personId` | body | `number` | yes | — |
| `startDate` | body | `date` | yes | — |
| `endDate` | body | `date` | yes | — |
| `roleStartDate` | body | `date` | no | Optional. When provided, updates the unfilled role's start date before creating the allocation. Must be set together with ResourcePlanning.Contracts.TaskAllocationRequest.RoleEndDate — supplying only one will fail validation. |
| `roleEndDate` | body | `date` | no | Optional. When provided, updates the unfilled role's end date before creating the allocation. Must be set together with ResourcePlanning.Contracts.TaskAllocationRequest.RoleStartDate — supplying only one will fail validation. |

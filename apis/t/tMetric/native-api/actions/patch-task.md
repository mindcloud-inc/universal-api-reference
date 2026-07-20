# Patch Task with TMetric

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/tasks/:taskId`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Patch Task](https://app.tmetric.com/api-docs/#/Tasks/patch-accounts-accountId-tasks-taskId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `assignee.id` | body | `number` | no | Assignee identifier. |
| `description` | body | `string` | no | Updated task description. |
| `dueDate` | body | `date` | no | Task due date. |
| `estimatedMinutes` | body | `number` | no | Estimated time in minutes. |
| `isCompleted` | body | `boolean` | no | Whether the task is completed. |
| `name` | body | `string` | no | Updated task name. |
| `project.id` | body | `number` | no | Project identifier. |
| `taskId` | path | `number` | yes | Task identifier. |

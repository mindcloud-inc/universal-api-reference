# Create Task with TMetric

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/tasks`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Create Task](https://app.tmetric.com/api-docs/#/Tasks/post-accounts-accountId-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `assignee.id` | body | `number` | no | Assignee identifier. |
| `dryRun` | query | `boolean` | no | Validate the task payload without saving. |
| `dueDate` | body | `date` | no | Task due date. |
| `estimatedMinutes` | body | `number` | no | Estimated time in minutes. |
| `isCompleted` | body | `boolean` | no | Whether the task is completed. |
| `name` | body | `string` | no | Task name. |
| `project.id` | body | `number` | no | Project identifier. |

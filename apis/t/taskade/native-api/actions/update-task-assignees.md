# Update Task Assignees with Taskade

Updates assignees for a Taskade task.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/tasks/:taskId/assignees`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Update Task Assignees](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task-assignees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |
| `handles[]` | body | `array<string>` | yes | Assignee handles. |

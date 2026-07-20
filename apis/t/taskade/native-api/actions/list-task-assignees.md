# List Task Assignees with Taskade

Retrieves assignees for a Taskade task.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks/:taskId/assignees`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List Task Assignees](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task-assignees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |

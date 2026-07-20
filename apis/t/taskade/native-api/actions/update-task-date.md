# Update Task Date with Taskade

Updates date details for a Taskade task.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/tasks/:taskId/date`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Update Task Date](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |
| `start.date` | body | `string` | yes | Start date. |
| `start.time` | body | `string` | yes | Start time. |
| `start.timezone` | body | `string` | yes | Start timezone. |
| `end.date` | body | `string` | yes | End date. |
| `end.time` | body | `string` | yes | End time. |
| `end.timezone` | body | `string` | yes | End timezone. |

# Get Task Date with Taskade

Retrieves date details for a Taskade task.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks/:taskId/date`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Get Task Date](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |

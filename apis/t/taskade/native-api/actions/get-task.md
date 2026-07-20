# Get Task with Taskade

Retrieves a task from a Taskade project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks/:taskId`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Get Task](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |

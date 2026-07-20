# Move Task with Taskade

Moves a task within a Taskade project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/tasks/:taskId/move`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Move Task](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/move-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |
| `target.taskId` | body | `string` | yes | Target task ID. |
| `target.position` | body | `string` | yes | Relative insertion position. |

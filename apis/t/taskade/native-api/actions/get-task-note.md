# Get Task Note with Taskade

Retrieves the note for a Taskade task.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks/:taskId/note`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Get Task Note](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |

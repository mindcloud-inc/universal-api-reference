# Create Task with Taskade

Creates a new task in a Taskade project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/tasks/`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Create Task](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `tasks[].content` | body | `string` | yes | Task content. |

# Update Task with Taskade

Updates an existing task in a Taskade project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/tasks/:taskId`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Update Task](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project ID. |
| `taskId` | path | `string` | yes | Task ID. |
| `content` | body | `string` | yes | Task content. |

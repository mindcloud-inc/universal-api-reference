# Create Task with Awork

Creates a task in Awork.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Create Task](https://developers.awork.com/apiv1/tasks/creates-a-new-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the task. |
| `baseType` | body | `string` | yes | Use private for a private task or projecttask for a project task. |
| `entityId` | body | `string` | no | Required for project tasks and must be the project ID. |
| `description` | body | `string` | no | The description of the task. |

# Deletes a task with Worksnaps

Deletes an existing task from a Worksnaps project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/tasks/{task_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Deletes a task](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the project that the task to be deleted is in |
| `task_id` | path | `string` | no | ID of the target task to be deleted |

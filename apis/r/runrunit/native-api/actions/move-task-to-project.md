# Move Task To Project with Runrun.it

Updates a task's project in Runrun.it.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:id/change_project`
- **Base URL:** `https://runrun.it/api/v1.0`
- **Official documentation:** [Move Task To Project](https://runrun.it/api/documentation#tasks-change-the-project-from-task-to-another)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id path parameter. |
| `project_id` | body | `number` | no | ID of the project the task belongs to |

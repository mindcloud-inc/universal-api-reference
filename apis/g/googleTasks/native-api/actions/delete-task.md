# Delete Task with Google Tasks

Deletes an existing task from Google Tasks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:tasklist/tasks/:task`
- **Base URL:** `https://tasks.googleapis.com/tasks/v1`
- **Official documentation:** [Delete Task](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tasklist` | path | `list` | yes |
| `task` | path | `string` | yes |

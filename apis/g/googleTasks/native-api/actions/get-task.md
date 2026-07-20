# Get Task with Google Tasks

Retrieves a task from Google Tasks.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:tasklist/tasks/:task`
- **Base URL:** `https://tasks.googleapis.com/tasks/v1`
- **Official documentation:** [Get Task](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tasklist` | path | `list` | yes |
| `task` | path | `string` | yes |

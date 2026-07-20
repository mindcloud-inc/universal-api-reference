# Update Task with Google Tasks

Updates an existing task in Google Tasks.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/lists/:tasklist/tasks/:task`
- **Base URL:** `https://tasks.googleapis.com/tasks/v1`
- **Official documentation:** [Update Task](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tasklist` | path | `list` | yes |
| `task` | path | `string` | yes |
| `title` | body | `string` | no |
| `notes` | body | `string` | no |
| `due` | body | `date` | no |
| `status` | body | `string` | no |
| `completed` | body | `date` | no |
| `clear` | query | `string` | no |
| `parent` | query | `string` | no |
| `previous` | query | `string` | no |

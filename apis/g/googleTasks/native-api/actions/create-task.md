# Create Task with Google Tasks

Creates a new task in Google Tasks.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:tasklist/tasks`
- **Base URL:** `https://tasks.googleapis.com/tasks/v1`
- **Official documentation:** [Create Task](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/insert)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tasklist` | path | `list` | yes |
| `title` | body | `string` | no |
| `notes` | body | `string` | no |
| `due` | body | `date` | no |
| `parent` | query | `string` | no |
| `previous` | query | `string` | no |

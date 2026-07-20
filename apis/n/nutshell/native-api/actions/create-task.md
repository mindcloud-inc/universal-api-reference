# Create Task with Nutshell

Creates a new task in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Create Task](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Title of the task. |
| `description` | body | `string` | no | Description of the task. |
| `dueTime` | body | `date` | no | Due time for the task. |
| `links.relatedEntity` | body | `string` | no | Entity ID to attach to the task. |
| `links.assignee` | body | `string` | no | User ID to assign to the task. |

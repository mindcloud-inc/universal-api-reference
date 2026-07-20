# Quick Add with Todoist

Creates a task in Todoist from quick-add text.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/quick`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Quick Add](https://developer.todoist.com/api/v1/#tag/Tasks/operation/quick_add_api_v1_tasks_quick_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Task content to add |
| `note` | body | `string` | no | Optional note content |
| `reminder` | body | `string` | no | Natural language reminder |
| `auto_reminder` | body | `boolean` | no | Enable automatic reminder inference |

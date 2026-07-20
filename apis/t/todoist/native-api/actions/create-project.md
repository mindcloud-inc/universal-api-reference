# Create Project with Todoist

Creates a new project in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Create Project](https://developer.todoist.com/api/v1/#tag/Projects/operation/create_project_api_v1_projects_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Project name. |
| `description` | body | `string` | no | Project description. |
| `parent_id` | body | `string` | no | Parent project identifier. |
| `color` | body | `string` | no | Project color. |
| `is_favorite` | body | `boolean` | no | Mark as favorite. |
| `view_style` | body | `string` | no | Project view style (list, board, or calendar). |
| `workspace_id` | body | `number` | no | Workspace identifier. |

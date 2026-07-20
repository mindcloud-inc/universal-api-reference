# Update Project with Todoist

Updates an existing project in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects/:project_id`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Update Project](https://developer.todoist.com/api/v1/#tag/Projects/operation/update_project_api_v1_projects__project_id__post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project identifier. |
| `name` | body | `string` | no | Project name. |
| `description` | body | `string` | no | Project description. |
| `color` | body | `string` | no | Project color. |
| `is_favorite` | body | `boolean` | no | Mark as favorite. |
| `view_style` | body | `string` | no | Project view style (list, board, or calendar). |

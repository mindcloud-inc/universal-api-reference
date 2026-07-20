# Get Project with Vimeo

Retrieves a project record from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/projects/:project_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Get Project](https://developer.vimeo.com/api/reference/folders#get_project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `project_id` | path | `number` | yes | The ID of the folder. |

# Delete Task with Toggl Track

Deletes an existing task from Toggl Track.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Delete Task](https://engineering.toggl.com/docs/track/api/tasks/#delete-workspaceprojecttask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |

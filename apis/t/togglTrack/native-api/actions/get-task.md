# Get Task with Toggl Track

Retrieves a task from Toggl Track.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Get Task](https://engineering.toggl.com/docs/track/api/tasks/#get-workspaceprojecttask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `project_id` | path | `number` | yes |
| `task_id` | path | `number` | yes |

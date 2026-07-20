# Delete Project with Toggl Track

Deletes an existing project from Toggl Track.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Delete Project](https://engineering.toggl.com/docs/track/api/projects/#delete-workspaceproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `project_id` | path | `number` | yes |

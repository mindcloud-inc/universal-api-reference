# Get Project with Toggl Track

Retrieves a project from Toggl Track.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Get Project](https://engineering.toggl.com/docs/track/api/projects/#get-workspaceproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `project_id` | path | `number` | yes |

# List Project Tasks with Toggl Track

Retrieves tasks for a Toggl Track project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id/tasks`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [List Project Tasks](https://engineering.toggl.com/docs/track/api/tasks/#get-workspaceprojecttasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `project_id` | path | `list<number>` | yes |
| `active` | query | `boolean` | no |

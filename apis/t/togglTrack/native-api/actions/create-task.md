# Create Task with Toggl Track

Creates a new task in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id/tasks`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Create Task](https://engineering.toggl.com/docs/track/api/tasks/#post-workspaceprojecttasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `project_id` | path | `list<number>` | yes |
| `name` | body | `string` | yes |
| `active` | body | `boolean` | no |

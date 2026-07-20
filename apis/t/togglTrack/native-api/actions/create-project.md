# Create Project with Toggl Track

Creates a new project in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v9/workspaces/:workspace_id/projects`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Create Project](https://engineering.toggl.com/docs/track/api/projects/#post-workspaceprojects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `name` | body | `string` | yes |
| `active` | body | `boolean` | no |
| `is_private` | body | `boolean` | no |
| `billable` | body | `boolean` | no |

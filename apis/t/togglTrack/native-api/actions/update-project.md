# Update Project with Toggl Track

Updates an existing project in Toggl Track.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Update Project](https://engineering.toggl.com/docs/track/api/projects/#put-workspaceproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `project_id` | path | `list<number>` | yes |
| `name` | body | `string` | no |
| `active` | body | `boolean` | no |
| `is_private` | body | `boolean` | no |
| `billable` | body | `boolean` | no |
| `client_id` | body | `list<number>` | no |
| `start_date` | body | `date` | no |
| `end_date` | body | `date` | no |
| `estimated_hours` | body | `number` | no |
| `color` | body | `string` | no |

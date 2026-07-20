# Update Task with Toggl Track

Updates an existing task in Toggl Track.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Update Task](https://engineering.toggl.com/docs/track/api/tasks/#put-workspaceprojecttask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `project_id` | path | `list<number>` | yes |
| `task_id` | path | `list<number>` | yes |
| `name` | body | `string` | no |
| `active` | body | `boolean` | no |
| `estimated_seconds` | body | `number` | no |
| `user_id` | body | `number` | no |
| `external_reference` | body | `string` | no |

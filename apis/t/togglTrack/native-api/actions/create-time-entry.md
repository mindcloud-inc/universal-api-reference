# Create Time Entry with Toggl Track

Creates a new time entry in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v9/workspaces/:workspace_id/time_entries`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Create Time Entry](https://engineering.toggl.com/docs/track/api/time_entries/#post-timeentries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `wid` | body | `number` | yes |
| `created_with` | body | `string` | yes |
| `start` | body | `date` | yes |
| `duration` | body | `number` | no |
| `description` | body | `string` | no |
| `project_id` | body | `number` | no |
| `task_id` | body | `number` | no |
| `billable` | body | `boolean` | no |
| `meta` | query | `boolean` | no |

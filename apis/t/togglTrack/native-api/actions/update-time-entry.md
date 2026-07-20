# Update Time Entry with Toggl Track

Updates an existing time entry in Toggl Track.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v9/workspaces/:workspace_id/time_entries/:time_entry_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Update Time Entry](https://engineering.toggl.com/docs/track/api/time_entries/#put-timeentries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `time_entry_id` | path | `list<number>` | yes |
| `description` | body | `string` | no |
| `start` | body | `date` | no |
| `stop` | body | `date` | no |
| `duration` | body | `number` | no |
| `project_id` | body | `list<number>` | no |
| `task_id` | body | `list<number>` | no |
| `billable` | body | `boolean` | no |
| `created_with` | body | `string` | no |
| `start_date` | body | `date` | no |
| `meta` | query | `boolean` | no |
| `include_sharing` | query | `boolean` | no |

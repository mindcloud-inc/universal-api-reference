# Delete Time Entry with Toggl Track

Deletes an existing time entry from Toggl Track.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v9/workspaces/:workspace_id/time_entries/:time_entry_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Delete Time Entry](https://engineering.toggl.com/docs/track/api/time_entries/#delete-timeentries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
| `time_entry_id` | path | `number` | yes |

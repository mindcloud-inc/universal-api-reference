# Stop Time Entry with Toggl Track

Stops an existing time entry in Toggl Track.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v9/workspaces/:workspace_id/time_entries/:time_entry_id/stop`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Stop Time Entry](https://engineering.toggl.com/docs/track/api/time_entries/#patch-stop-timeentry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `time_entry_id` | path | `list<number>` | yes |

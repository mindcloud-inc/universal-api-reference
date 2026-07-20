# Get Time Entry By ID with Toggl Track

Retrieves a time entry by ID from Toggl Track.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v9/me/time_entries/:time_entry_id`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Get Time Entry By ID](https://engineering.toggl.com/docs/track/api/time_entries/#get-get-a-time-entry-by-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `time_entry_id` | path | `number` | yes |

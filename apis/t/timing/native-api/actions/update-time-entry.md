# Update Time Entry with Timing

Updates an existing time entry in Timing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/time-entries/:time_entry_id`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Update Time Entry](https://web.timingapp.com/docs/#time-entries-PUTapi-v1-time-entries--time_entry_id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_entry_id` | path | `string` | yes | The Timing time entry ID to update. |
| `title` | body | `string` | no | — |

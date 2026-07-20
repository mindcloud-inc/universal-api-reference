# Delete Time Entry with Timing

Deletes an existing time entry from Timing.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/time-entries/:time_entry_id`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Delete Time Entry](https://web.timingapp.com/docs/#time-entries-DELETEapi-v1-time-entries--time_entry_id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_entry_id` | path | `string` | yes | The Timing time entry ID to delete. |

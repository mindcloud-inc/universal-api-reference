# Delete Time Entry with ProProfs Project

Deletes an existing time entry from ProProfs Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/time_entries/{{entry_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Delete Time Entry](https://help.proprofsproject.com/time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entry_id` | path | `string` | yes | The time entry ID to delete. |

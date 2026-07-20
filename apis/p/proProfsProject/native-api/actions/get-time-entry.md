# Get Time Entry with ProProfs Project

Retrieves a time entry from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/time_entries/{{entry_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Get Time Entry](https://help.proprofsproject.com/time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entry_id` | path | `string` | yes | The time entry ID to fetch. |

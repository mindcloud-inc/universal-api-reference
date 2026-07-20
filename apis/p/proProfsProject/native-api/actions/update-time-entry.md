# Update Time Entry with ProProfs Project

Updates an existing time entry in ProProfs Project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/time_entries/{{entry_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Time Entry](https://help.proprofsproject.com/time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated time entry description. |
| `entry_id` | path | `string` | yes | The time entry ID to update. |
| `seconds` | body | `string` | yes | The total seconds for the updated entry. |

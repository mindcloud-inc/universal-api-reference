# Create Time Entry with ProProfs Project

Creates a new time entry in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/time_entries/{{task_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Time Entry](https://help.proprofsproject.com/time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The time entry description. |
| `seconds` | body | `string` | yes | Total tracked seconds for the entry. |
| `task_id` | path | `string` | yes | The parent task ID. |

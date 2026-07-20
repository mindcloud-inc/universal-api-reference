# List Subtasks with ProProfs Project

Retrieves a list of subtasks from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/subtasks`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Subtasks](https://help.proprofsproject.com/subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | no | Filter subtasks by parent task ID. |
| `team_id` | query | `string` | no | Filter subtasks by team ID. |
| `user_id` | query | `string` | no | Filter subtasks by user ID. |

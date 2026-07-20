# Create Subtask with ProProfs Project

Creates a new subtask in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/subtasks/{{task_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Subtask](https://help.proprofsproject.com/subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subtask_name` | body | `string` | yes | The subtask name. |
| `task_id` | path | `string` | yes | The parent task ID. |

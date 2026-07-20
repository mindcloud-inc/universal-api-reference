# Update Subtask with ProProfs Project

Updates an existing subtask in ProProfs Project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/subtasks/{{subtask_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Subtask](https://help.proprofsproject.com/subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subtask_id` | path | `string` | yes | The subtask ID to update. |
| `subtask_name` | body | `string` | no | The updated subtask name. |

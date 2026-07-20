# Delete Subtask with ProProfs Project

Deletes an existing subtask from ProProfs Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subtasks/{{subtask_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Delete Subtask](https://help.proprofsproject.com/subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subtask_id` | path | `string` | yes | The subtask ID to delete. |

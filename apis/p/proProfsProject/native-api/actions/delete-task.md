# Delete Task with ProProfs Project

Deletes an existing task from ProProfs Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/{{task_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Delete Task](https://help.proprofsproject.com/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The task ID to delete. |

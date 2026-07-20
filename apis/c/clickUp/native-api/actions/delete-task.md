# Delete Task with ClickUp

Delete a task from Workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `task/:task_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Delete Task](https://developer.clickup.com/reference/deletetask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_task_ids` | query | `boolean` | no | If you want to reference a task by its custom task id, this value must be true. |
| `team_id` | query | `list` | no | When the custom_task_ids parameter is set to true, the Workspace ID must be provided using the team_id parameter. For example: custom_task_ids=true&team_id=123. |
| `task_id` | path | `string` | yes | — |

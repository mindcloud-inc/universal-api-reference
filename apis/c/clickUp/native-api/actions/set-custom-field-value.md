# Set Custom Field Value with ClickUp

Add data to a Custom field on a task.

## Endpoint

- **Method:** `POST`
- **Path:** `task/:task_id/field/:field_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Set Custom Field Value](https://developer.clickup.com/reference/setcustomfieldvalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | — |
| `field_id` | path | `string` | yes | — |
| `customTaskids` | query | `boolean` | no | If you want to reference a task by its Custom Task ID, this value must be true. Format: `toggle`. |
| `teamId` | query | `list` | no | When the custom_task_ids parameter is set to true, the Workspace ID must be provided using the team_id parameter.   For example: custom_task_ids=true&team_id=123. |

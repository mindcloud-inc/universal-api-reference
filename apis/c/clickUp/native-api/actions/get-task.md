# Get Task with ClickUp

Retrieves details for a task from ClickUp.

## Endpoint

- **Method:** `GET`
- **Path:** `task/:task_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Get Task](https://developer.clickup.com/reference/gettask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_task_ids` | query | `boolean` | no | — |
| `team_id` | query | `list` | no | — |
| `include_markdown_description` | query | `boolean` | no | Format: `toggle`. |
| `task_id` | path | `string` | yes | — |

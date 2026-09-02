# Update Task with ClickUp

Updates an existing task in ClickUp.

## Endpoint

- **Method:** `PUT`
- **Path:** `task/:task_id`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Update Task](https://developer.clickup.com/reference/updatetask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignees.add[]` | body | `array<number>` | no | — |
| `custom_item_id` | body | `number` | no | To convert an item using a custom task type into a task, send 'null'.  To update this task to be a Milestone, send a value of 1.  To use a custom task type, send the custom task type ID as defined in your Workspace, such as 2. |
| `group_assignees.add[]` | body | `array<number>` | no | — |
| `markdown_content` | body | `string` | no | — |
| `watchers.add[]` | body | `array<number>` | no | — |
| `assignees.rem[]` | body | `array<number>` | no | — |
| `group_assignees.rem[]` | body | `array<number>` | no | — |
| `name` | body | `string` | no | — |
| `watchers.rem[]` | body | `array<number>` | no | — |
| `description` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `priority` | body | `list` | no | — |
| `due_date` | body | `date` | no | — |
| `due_date_time` | body | `boolean` | no | Format: `toggle`. |
| `start_date` | body | `date` | no | — |
| `start_date_time` | body | `boolean` | no | Format: `toggle`. |
| `points` | body | `number` | no | — |
| `archived` | body | `boolean` | no | Format: `toggle`. |
| `parent` | body | `string` | no | You can move a subtask to another parent task by including "parent" with a valid task id.  You cannot convert a subtask to a task by setting "parent" to null. |
| `time_estimate` | body | `number` | no | Time in milliseconds |
| `assignees` | body | `object` | no | — |
| `group_assignees` | body | `object` | no | — |
| `watchers` | body | `object` | no | — |
| `custom_task_ids` | query | `boolean` | no | Format: `toggle`. |
| `task_id` | path | `string` | yes | — |
| `team_id` | query | `list` | no | — |

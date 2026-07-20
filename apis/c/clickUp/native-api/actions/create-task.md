# Create Task with ClickUp

Create a new task.

## Endpoint

- **Method:** `POST`
- **Path:** `list/:list_id/task`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create Task](https://developer.clickup.com/reference/createtask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_estimate` | body | `number` | no | Time estimate in milliseconds |
| `custom_fields[].id` | body | `string` | no | — |
| `list_id` | path | `string` | yes | — |
| `custom_fields[].value` | body | `string` | no | — |
| `custom_fields` | body | `array<object>` | no | — |
| `custom_item_id` | body | `number` | no | To create a task that doesn't use a custom task type, either don't include this field in the request body, or send 'null'.  To create this task as a Milestone, send a value of 1.  To use a custom task type, send the custom task type ID as defined in your Workspace, such as 2. |
| `archived` | body | `boolean` | no | Format: `toggle`. |
| `assignees[]` | body | `array<number>` | no | — |
| `check_required_custom_fields` | body | `boolean` | no | Format: `toggle`. |
| `description` | body | `string` | no | — |
| `due_date` | body | `date` | no | — |
| `due_date_time` | body | `boolean` | no | Format: `toggle`. |
| `group_assignees` | body | `array<number>` | no | — |
| `links_to` | body | `string` | no | — |
| `markdown_content` | body | `string` | no | — |
| `name` | body | `string` | yes | — |
| `notify_all` | body | `boolean` | no | Format: `toggle`. |
| `parent` | body | `string` | no | — |
| `points` | body | `number` | no | — |
| `priority` | body | `list` | no | — |
| `start_date` | body | `date` | no | — |
| `start_date_time` | body | `boolean` | no | Format: `toggle`. |
| `status` | body | `string` | no | — |
| `tags` | body | `array<string>` | no | — |

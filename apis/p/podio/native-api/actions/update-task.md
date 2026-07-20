# Update Task with Podio

Updates an existing task in Podio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/task/:task_id`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Update Task](https://developers.podio.com/doc/tasks/update-task-10583674)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The ID of the task to update. |
| `text` | body | `string` | no | The updated task title text. |
| `description` | body | `string` | no | The updated task description. |
| `due_date` | body | `date` | no | The new due date in the user's timezone. |
| `due_time` | body | `string` | no | The new due time in the user's timezone. |
| `responsible` | body | `string` | no | The user ID of the responsible user. |
| `private` | body | `boolean` | no | Whether the task should be private. |
| `ref_type` | body | `string` | no | The reference type for the task. |
| `ref_id` | body | `string` | no | The reference ID for the task. |
| `completed` | body | `boolean` | no | Mark the task as completed or not completed. |
| `labels[]` | body | `array<string>` | no | A list of label IDs or label texts for the task. |
| `file_ids[]` | body | `array<string>` | no | A list of uploaded file IDs to attach to the task. |
| `reminder` | body | `object` | no | Optional reminder settings for the task. |
| `reminder.remind_delta` | body | `number` | no | Minutes before the due date to trigger the reminder. Leave empty to clear the existing reminder. |
| `hook` | query | `boolean` | no | Run Podio hooks for the change. |
| `silent` | query | `boolean` | no | Suppress stream bumping and notifications for the update. |

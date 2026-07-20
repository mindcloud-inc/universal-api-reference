# Update Task with Kommo

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Update Task](https://developers.kommo.com/reference/edit-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task ID. |
| `responsible_user_id` | body | `number` | no | Responsible user ID. |
| `entity_id` | body | `number` | no | Related entity ID. |
| `entity_type` | body | `string` | no | Related entity type. |
| `is_completed` | body | `boolean` | no | Whether the task is completed. |
| `task_type_id` | body | `number` | no | Task type ID. |
| `text` | body | `string` | no | Task text. |
| `duration` | body | `number` | no | Task duration. |
| `complete_till` | body | `number` | no | Task deadline timestamp. |
| `result` | body | `object` | no | Task result payload. |
| `request_id` | body | `string` | no | Request identifier. |

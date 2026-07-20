# Create Task with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Task](https://developers.kommo.com/reference/add-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `responsible_user_id` | body | `number` | no | Responsible user ID. |
| `entity_id` | body | `number` | no | Related entity ID. |
| `entity_type` | body | `string` | no | Related entity type. |
| `is_completed` | body | `boolean` | no | Whether the task is completed. |
| `task_type_id` | body | `number` | no | Task type ID. |
| `text` | body | `string` | yes | Task text. |
| `duration` | body | `number` | no | Task duration. |
| `complete_till` | body | `number` | yes | Task deadline timestamp. |
| `result` | body | `object` | no | Task result payload. |
| `request_id` | body | `string` | no | Request identifier. |

# Update Task with Keap

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/{task_id}`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Update Task](https://developer.keap.com/docs/restv2/#tag/Task/operation/updateTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_to_user_id` | body | `string` | no | — |
| `completed` | body | `string` | no | — |
| `completion_time` | body | `string` | no | — |
| `contact_id` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `due_time` | body | `string` | no | — |
| `priority` | body | `string` | no | — |
| `remind_time_mins` | body | `string` | no | — |
| `task_id` | path | `string` | yes | The unique identifier of the task. |
| `title` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `update_mask` | query | `string` | no | — |

# Create Task with Keap

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Create Task](https://developer.keap.com/docs/restv2/#tag/Task/operation/createTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assigned_to_user_id` | body | `string` | yes |
| `completed` | body | `string` | no |
| `completion_time` | body | `string` | no |
| `contact_id` | body | `string` | no |
| `description` | body | `string` | no |
| `due_time` | body | `string` | no |
| `priority` | body | `string` | no |
| `remind_time_mins` | body | `string` | no |
| `title` | body | `string` | no |
| `type` | body | `string` | no |

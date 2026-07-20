# Update Task with Freshworks CRM

Updates an existing task in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/tasks/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Task](https://developers.freshworks.com/crm/api/#update_task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `task` | body | `object` | yes |
| `task.description` | body | `string` | no |
| `task.due_date` | body | `string` | no |
| `task.owner_id` | body | `number` | no |
| `task.targetable_id` | body | `number` | no |
| `task.targetable_type` | body | `string` | no |
| `task.title` | body | `string` | no |

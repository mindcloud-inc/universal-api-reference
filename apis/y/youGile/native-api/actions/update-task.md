# Update task with YouGile

Updates an existing task in YouGile.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Update task](https://ru.yougile.com/api-v2#/operations/TaskController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The YouGile task ID. |
| `title` | body | `string` | no | The updated task title. |
| `columnId` | body | `string` | no | The column that owns the task. |
| `description` | body | `string` | no | The updated task description. |
| `archived` | body | `boolean` | no | Mark the task as archived. |
| `completed` | body | `boolean` | no | Mark the task as completed. |
| `deleted` | body | `boolean` | no | Mark the task as deleted. |

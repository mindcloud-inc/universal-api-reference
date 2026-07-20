# Create task with YouGile

Creates a new task in YouGile.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Create task](https://ru.yougile.com/api-v2#/operations/TaskController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The task title. |
| `columnId` | body | `string` | no | The column that owns the task. |
| `description` | body | `string` | no | The task description. |
| `archived` | body | `boolean` | no | Create the task as archived. |
| `completed` | body | `boolean` | no | Create the task as completed. |

# Update Task with Lunatask

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Update Task](https://lunatask.app/api/tasks-api/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the task to update |
| `name` | body | `string` | no | The new name of the task |
| `note` | body | `string` | no | The new note of the task in Markdown |
| `status` | body | `string` | no | The new status of the task |
| `motivation` | body | `string` | no | The new motivation value of the task |
| `scheduled_on` | body | `date` | no | ISO-8601 formatted date the task is scheduled on |

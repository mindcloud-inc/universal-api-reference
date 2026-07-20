# Create Task with Cogmento CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/`
- **Base URL:** `https://api.freecrm.com/api/1`
- **Official documentation:** [Create Task](https://api.cogmento.com/static/swagger/index.html#/Tasks/post_tasks_)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title of the task. |
| `description` | body | `string` | no | A description of the task. |
| `due_date` | body | `date` | no | The task deadline, formatted YYYY-MM-DD. |
| `assigned_to[]` | body | `array<object>` | no | Array of assignee user reference objects. |
| `deal` | body | `object` | no | Deal reference object associated with the task. |
| `contact` | body | `object` | no | Contact reference object associated with the task. |

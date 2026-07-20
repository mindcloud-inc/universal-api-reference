# Create Task with Podio

Creates a new task in Podio.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Create Task](https://developers.podio.com/doc/tasks/create-task-22419)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text of the task. |
| `description` | body | `string` | no | Description of the task. |
| `due_date` | body | `date` | no | Due date in YYYY-MM-DD format. |
| `due_time` | body | `string` | no | Time of the due date in HH:MM format. |
| `due_on` | body | `string` | no | — |
| `ref_type` | body | `string` | no | — |
| `private` | body | `boolean` | no | True to make the task private. |
| `ref_id` | body | `number` | no | — |
| `responsible[]` | body | `array<number>` | no | User id, auth object, or list of user ids to assign. |
| `hook` | query | `boolean` | no | — |
| `silent` | query | `boolean` | no | — |
| `external_id` | body | `string` | no | — |
| `file_ids[]` | body | `array<number>` | no | — |
| `labels[]` | body | `array<string>` | no | — |
| `label_ids[]` | body | `array<number>` | no | — |
| `reminder` | body | `object` | no | — |
| `recurrence` | body | `object` | no | — |

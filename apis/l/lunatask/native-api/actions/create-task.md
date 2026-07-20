# Create Task with Lunatask

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Create Task](https://lunatask.app/api/tasks-api/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `area_id` | body | `string` | yes | The Area ID of the list where the task should be created |
| `goal_id` | body | `string` | no | The ID of the goal where the task should be created |
| `name` | body | `string` | no | The name of the task |
| `note` | body | `string` | no | The note attached to the task in Markdown |
| `status` | body | `string` | no | The status of the task |
| `motivation` | body | `string` | no | The motivation value of the task |
| `eisenhower` | body | `number` | no | The quadrant on the Eisenhower matrix |
| `estimate` | body | `number` | no | The estimate of the task in minutes |
| `priority` | body | `number` | no | Priority of the task |
| `scheduled_on` | body | `date` | no | ISO-8601 formatted date the task is scheduled on |
| `completed_at` | body | `date` | no | ISO-8601 formatted time when the task was completed |
| `source` | body | `string` | no | Identification of the external system where the task is coming from |
| `source_id` | body | `string` | no | The ID of the record in the external system |

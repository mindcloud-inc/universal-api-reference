# Update task with OkoCRM

Updates an existing task in OkoCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/[:task_id]/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Update task](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `executor_id` | body | `string` | no | Updated assignee ID. |
| `task_id` | path | `number` | yes | The OkoCRM task ID. |
| `text` | body | `string` | no | Updated task text. |

# Delete Task with Kanban Tool

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:task_id.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Delete Task](https://kanbantool.com/developer/api-v3#deleting-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | Kanban Tool task ID. |

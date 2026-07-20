# Get a Task with Worksnaps

Retrieves a task from a Worksnaps project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/tasks/{task_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get a Task](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `task_id` | path | `string` | no | ID of the target task that needs to be fetched |

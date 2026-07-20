# Update a Task with Worksnaps

Updates an existing task in a Worksnaps project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{project_id}/tasks/{task_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Update a Task](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the project that the task to be updated is in |
| `task_id` | path | `string` | no | ID of the target task that needs to be updated. |

# Delete a Task Assignment by ID with Worksnaps

Deletes an existing task assignment from Worksnaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/task_assignments/{task_assignment_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Delete a Task Assignment by ID](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `task_assignment_id` | path | `string` | no | ID of the task assignment to be deleted |

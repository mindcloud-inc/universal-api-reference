# Delete a task assignment with Worksnaps

Deletes an existing task assignment from Worksnaps.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/task_assignments.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Delete a task assignment](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `task_id` | query | `string` | no | ID of the target task |
| `user_id` | query | `string` | no | ID of the target user that need to be unassigned the specified task |

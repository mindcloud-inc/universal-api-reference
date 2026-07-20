# Get a task assignment with Worksnaps

Retrieves a task assignment from a Worksnaps project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/task_assignments/{task_assignment_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get a task assignment](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project |
| `task_assignment_id` | path | `string` | no | ID of the task assignment to be fetched |

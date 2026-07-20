# Create a task assignment (i.e., assign a user to a task) with Worksnaps

Creates a task assignment in a Worksnaps project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/task_assignments.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Create a task assignment (i.e., assign a user to a task)](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project that the task is in |

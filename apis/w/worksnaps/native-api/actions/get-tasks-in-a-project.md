# Get Tasks In a Project with Worksnaps

Retrieves tasks in a specific Worksnaps project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/tasks.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Get Tasks In a Project](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | ID of the target project from which the tasks are fetched |

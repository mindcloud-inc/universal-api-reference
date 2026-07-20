# Create a Task with Worksnaps

Creates a new task in a Worksnaps project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/tasks.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Create a Task](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | path | `string` | no | ID of the target project in which the task is created |

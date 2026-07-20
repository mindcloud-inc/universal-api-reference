# Update Task with Iris Dfir

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/cases/:case_identifier/tasks/:identifier`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Update Task](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_(identifier)_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_identifier` | path | `number` | yes | IRIS case identifier. |
| `identifier` | path | `number` | yes | IRIS task identifier. |
| `task_assignees_id[]` | body | `array<number>` | yes | IRIS task assignee identifier. Send multiple values as a array. |
| `task_description` | body | `string` | no | Optional updated task description. |
| `task_status_id` | body | `number` | yes | IRIS task status identifier. |
| `task_tags` | body | `string` | no | Optional updated comma-separated task tags. |
| `task_title` | body | `string` | yes | Title of the task. |

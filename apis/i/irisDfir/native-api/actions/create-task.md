# Create Task with Iris Dfir

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/cases/:case_identifier/tasks`
- **Base URL:** `https://v200.beta.dfir-iris.org`
- **Official documentation:** [Create Task](https://docs.dfir-iris.org/latest/_static/iris_api_reference_v2.1.0.html#tag/Tasks/operation/api_v2_cases_(case_identifier)_tasks_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_identifier` | path | `number` | yes | IRIS case identifier. |
| `task_assignees_id[]` | body | `array<number>` | yes | IRIS task assignee identifier. Send multiple values as a array. |
| `task_description` | body | `string` | no | Optional task description. |
| `task_status_id` | body | `number` | yes | IRIS task status identifier. |
| `task_tags` | body | `string` | no | Optional comma-separated task tags. |
| `task_title` | body | `string` | yes | Title of the task. |

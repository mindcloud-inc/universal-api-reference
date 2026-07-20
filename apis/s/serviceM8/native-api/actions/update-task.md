# Update Task with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/task/:uuid.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Update Task](https://developer.servicem8.com/reference/updatetasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the Task |
| `name` | body | `string` | yes | The name or title of the task. |
| `task_details` | body | `string` | no | Detailed description of the task. |
| `due_date` | body | `date` | no | The date by which the task should be completed. |
| `related_object` | body | `string` | yes | The object class this task is related to. |
| `related_object_uuid` | body | `string` | yes | UUID of the specific object instance this task is related to. |
| `assigned_to_staff_uuid` | body | `string` | no | UUID of the staff member assigned to complete this task. |
| `task_complete` | body | `string` | no | Whether the task has been completed. |
| `completed_timestamp` | body | `date` | no | The date and time when the task was marked as complete. |
| `completed_by_staff_uuid` | body | `string` | no | UUID of the staff member who marked the task as complete. |
| `created_by_staff_uuid` | body | `string` | no | UUID of the staff member who created the task. |

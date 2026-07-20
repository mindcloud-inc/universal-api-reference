# Create Task Assignment with DataScope Forms

Creates a task assignment in DataScope Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/assign_task`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [Create Task Assignment](https://dscope.github.io/docs/#create-task-assign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `c_code` | query | `string` | no | Company tax ID or code of the location. |
| `c_name` | query | `string` | no | Company name of the location. |
| `code` | query | `string` | no | Code to identify the task. |
| `date` | query | `string` | yes | Date and time of the assigned task in YYYY-mm-dd HH:MM format. |
| `form_id` | query | `number` | yes | Internal identifier of the form to assign. |
| `gap` | query | `number` | no | Hours available to perform the task. |
| `l_code` | query | `string` | no | Code of the location for the task. |
| `l_email` | query | `string` | no | Email address of the location. |
| `l_phone` | query | `string` | no | Phone number of the location. |
| `latitude` | query | `number` | no | Latitude of the location. |
| `location_address` | query | `string` | no | Address of the location. |
| `location_name` | query | `string` | no | Name of the location when it needs to be created or updated. |
| `longitude` | query | `number` | no | Longitude of the location. |
| `task_instruction` | query | `string` | no | Instruction shown on the assigned task. |
| `user_id` | query | `string` | yes | Email address of the user assigned to the task. |

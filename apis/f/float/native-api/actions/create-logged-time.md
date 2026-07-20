# Create Logged Time with Float

Creates a new logged time entry in Float.

## Endpoint

- **Method:** `POST`
- **Path:** `/logged-time`
- **Base URL:** `https://api.float.com/v3`
- **Official documentation:** [Create Logged Time](https://developer.float.com/api_reference.html#Logged_Time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `people_id` | body | `number` | yes | The ID of the person for the logged time entry |
| `date` | body | `string` | yes | Date of the logged time entry |
| `reference_date` | body | `string` | no | The date on which to suppress a matching logged time suggestion |
| `hours` | body | `number` | yes | Total hours of the logged time entry |
| `notes` | body | `string` | no | Additional notes about this logged time entry |
| `project_id` | body | `number` | yes | The ID of the project on which this entry was logged |
| `phase_id` | body | `number` | no | The ID of the project phase for which this entry was logged |
| `task_id` | body | `number` | no | The ID of a scheduled allocation linked to this entry |
| `task_name` | body | `string` | no | The name of the project task against which this entry was logged |
| `task_meta_id` | body | `number` | no | The ID of the associated project task |

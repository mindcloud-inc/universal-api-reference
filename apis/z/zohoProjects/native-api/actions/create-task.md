# Create Task with Zoho Projects

Creates a new task in Zoho Projects.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasks`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Create Task](https://projectsapi.zoho.com/api-docs#tasks_create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `name` | body | `string` | yes | Task name. |
| `description` | body | `string` | no | Task description. |
| `tasklist.id` | body | `string` | no | Task list ID. |
| `parental_info.parent_task_id` | body | `string` | no | Parent task ID for subtask creation. |
| `status.id` | body | `string` | no | Task status ID. |
| `priority` | body | `string` | no | Task priority. |
| `start_date` | body | `string` | no | Task start date. |
| `end_date` | body | `string` | no | Task end date. |
| `duration.value` | body | `string` | no | Task duration value. |
| `duration.type` | body | `string` | no | Task duration unit. |
| `completion_percentage` | body | `number` | no | Task completion percentage. |
| `billing_type` | body | `string` | no | Task billing type. |

# Update Task with Cerbo

Updates an existing task in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/task/:task_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Task](https://docs.cer.bo/#tag/Tasks/operation/updateTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | no | — |
| `dr_id` | body | `number` | no | A valid ID of a non-archived, non-resource user who the task is being added for. |
| `subject` | body | `string` | no | — |
| `priority` | body | `string` | no | — |
| `notes` | body | `string` | no | — |
| `pt_id` | body | `number` | no | A valid ID of a non-archived patient to associate with the task. |
| `due_date` | body | `date` | no | A time stamp (YYYY-MM-DD HH:MM:SS format) representing the due date for this task. |
| `remind_minutes_before` | body | `number` | no | Represents the number of minutes before your due date to remind the user of the task (due_date must be set). |
| `completed_on` | body | `date` | no | Marks the task as complete or incomplete. Pass a valid timestamp (YYYY-MM-DD HH:MM:SS format) to mark complete. The date must be today or in the past — future dates are rejected. Pass null or false to reset the task to incomplete. |
| `associated_resource_type` | body | `string` | no | Links the task to a resource type (encounter note or document). Pass null or empty to unlink. If set, associated_resource_id must also be provided. If a pt_id is set, the linked resource must belong to the same patient. |
| `associated_resource_id` | body | `number` | no | The ID of the linked resource. Required when associated_resource_type is set. |

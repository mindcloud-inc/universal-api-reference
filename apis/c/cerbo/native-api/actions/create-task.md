# Create Task with Cerbo

Creates a new task in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Task](https://docs.cer.bo/#tag/Tasks/operation/createTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dr_id` | body | `number` | yes | A valid ID of a non-archived, non-resource user who the task is being added for. |
| `subject` | body | `string` | yes | — |
| `priority` | body | `string` | yes | — |
| `notes` | body | `string` | no | — |
| `pt_id` | body | `number` | no | A valid ID of a non-archived patient to associate with the task. |
| `due_date` | body | `date` | no | A time stamp (YYYY-MM-DD HH:MM:SS format) representing the due date for this task. |
| `remind_minutes_before` | body | `number` | no | Represents the number of minutes before your due date to remind the user of the task (due_date must be set). |

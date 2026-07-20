# Update Time Entry with Trackabi

Updates an existing time entry in Trackabi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/time-entry/:timeEntryId`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Update Time Entry](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_entry_id` | path | `number` | yes | The unique ID of the time entry. |
| `member_id` | body | `number` | no | Member ID. Do not use together with email. |
| `email` | body | `string` | no | Member email. Do not use together with member ID. |
| `client_id` | body | `number` | no | Client ID. Do not use together with client name. |
| `client_name` | body | `string` | no | Client name. Do not use together with client ID. |
| `project_id` | body | `number` | no | Project ID. Do not use together with project name. |
| `project_name` | body | `string` | no | Project name. Do not use together with project ID. |
| `task_id` | body | `number` | no | Task ID. Do not use together with task name. |
| `task_name` | body | `string` | no | Task name. Do not use together with task ID. |
| `date_logged` | body | `date` | no | Date logged in YYYY-MM-DD format. |
| `description` | body | `string` | no | Description of work. |
| `logged_time` | body | `string` | no | Logged time in HH:MM:SS format. |
| `billable` | body | `string` | no | Billable time in HH:MM:SS format. |
| `start_time` | body | `string` | no | Start time in HH:MM:SS format. |
| `end_time` | body | `string` | no | End time in HH:MM:SS format. |
| `time_type` | body | `string` | no | Name of time type. |

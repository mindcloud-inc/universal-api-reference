# Update Oncall Schedule with Pinghome

Updates an existing on-call schedule in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/incident-cmd/v1/team/:id/schedule`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Oncall Schedule](https://docs.pinghome.io/incident-management/incident-schedule-management/update-oncall-schedule/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the team. |
| `team_member_id` | body | `string` | yes | The unique ID of the team member assigned to the schedule. |
| `created_at` | body | `string` | yes | The creation timestamp identifying the schedule. |
| `start_date` | body | `string` | no | The schedule start date in ISO-8601 format. |
| `end_date` | body | `string` | no | The schedule end date in ISO-8601 format. |
| `months_of_year` | body | `string` | no | Months of the year included in the recurrence. |
| `weeks_of_month` | body | `string` | no | Weeks of the month included in the recurrence. |
| `week_days` | body | `string` | no | Weekdays included in the recurrence. |
| `start_time` | body | `string` | no | The schedule start time in HH:mm:ss format. |
| `end_time` | body | `string` | no | The schedule end time in HH:mm:ss format. |

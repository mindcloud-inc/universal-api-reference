# Create Oncall Schedule with Pinghome

Creates a new on-call schedule in Pinghome.

## Endpoint

- **Method:** `POST`
- **Path:** `/incident-cmd/v1/team/:id/schedule`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Create Oncall Schedule](https://docs.pinghome.io/incident-management/incident-schedule-management/create-oncall-schedule/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The team ID for the schedule. |
| `team_member_id` | body | `string` | yes | The team member assigned to the schedule. |
| `start_date` | body | `string` | yes | The schedule start date in ISO-8601 format. |
| `end_date` | body | `string` | yes | The schedule end date in ISO-8601 format. |
| `months_of_year` | body | `string<number>` | yes | Months of the year included in the recurrence. |
| `weeks_of_month` | body | `string<number>` | yes | Weeks of the month included in the recurrence. |
| `week_days` | body | `string<number>` | yes | Weekdays included in the recurrence. |
| `start_time` | body | `string` | yes | The schedule start time in HH:mm:ss format. |
| `end_time` | body | `string` | yes | The schedule end time in HH:mm:ss format. |

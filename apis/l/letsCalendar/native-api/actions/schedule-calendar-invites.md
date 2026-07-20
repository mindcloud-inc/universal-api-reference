# Schedule Calendar Invites with Let's Calendar

Schedules calendar invites in Let's Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `schedule-invite`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Schedule Calendar Invites](https://panel.letscalendar.com/docs#apis-POSTapi-lc-schedule-invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
| `schedule_date` | body | `string` | yes | The date for scheduling in Y-m-d format. |
| `schedule_time` | body | `string` | yes | The time for scheduling in H:i format. |
| `timezone` | body | `string` | yes | The timezone for the schedule. |

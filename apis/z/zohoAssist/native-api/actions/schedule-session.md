# Schedule Session with Zoho Assist

Schedules a remote support or screen sharing session in Zoho Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/session/schedule`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Schedule Session](https://www.zoho.com/assist/api/schedulesession.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the scheduled session. |
| `notes` | body | `string` | no | Description or notes for the scheduled session. |
| `customer_email` | body | `string` | yes | Email address to invite to the scheduled session. |
| `schedule_time` | body | `number` | yes | Scheduled start time in Unix milliseconds. |
| `schedule_upto` | body | `number` | yes | Estimated session end time in Unix milliseconds. |
| `utc_offset` | body | `string` | yes | UTC offset for the scheduled time zone. |
| `time_zone` | body | `string` | yes | IANA time zone for the scheduled session. |
| `reminder` | body | `number` | yes | Reminder offset for the scheduled session. |
| `department_id` | body | `string` | yes | Department in which the session should be scheduled. |

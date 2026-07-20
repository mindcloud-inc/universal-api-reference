# Create SMS Appointment Reminder with Cerbo

Creates a new SMS appointment reminder in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments/:appointment_id/reminders/sms`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create SMS Appointment Reminder](https://docs.cer.bo/#tag/Appointment-Reminders/operation/createSmsAppointmentReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_id` | path | `number` | yes | ID of the appointment |
| `scheduled_datetime` | body | `string` | yes | Datetime for the reminder to be sent. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `text` | body | `string` | yes | Body of the reminder SMS. |

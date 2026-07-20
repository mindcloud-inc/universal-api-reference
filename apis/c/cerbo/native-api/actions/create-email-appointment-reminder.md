# Create Email Appointment Reminder with Cerbo

Creates a new email appointment reminder in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments/:appointment_id/reminders/email`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Email Appointment Reminder](https://docs.cer.bo/#tag/Appointment-Reminders/operation/createEmailAppointmentReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_id` | path | `number` | yes | ID of the appointment |
| `scheduled_datetime` | body | `string` | yes | Datetime for the reminder to be sent. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `subject` | body | `string` | yes | Subject for the reminder email. |
| `text` | body | `string` | yes | Body of the reminder email. |

# List Appointment Reminders with Cerbo

Retrieves appointment reminders from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/appointments/:appointment_id/reminders`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Appointment Reminders](https://docs.cer.bo/#tag/Appointment-Reminders/operation/listAppointmentReminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_id` | path | `number` | yes | ID of the appointment |

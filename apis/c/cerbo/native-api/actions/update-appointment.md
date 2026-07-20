# Update Appointment with Cerbo

Updates an existing appointment in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/appointments/:appointment_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Appointment](https://docs.cer.bo/#tag/Appointments/operation/updateAppointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_id` | path | `number` | yes | Appointment identifier. |
| `start_date_time` | body | `string` | no | Starting datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `end_date_time` | body | `string` | no | Ending datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `provider_ids[]` | body | `array<number>` | no | An array of provider identifiers associated with this appointment. |
| `pt_id` | body | `number` | no | A patient identifier associated with this appointment. |
| `appointment_type` | body | `string` | no | Valid appointment type `name`. |
| `title` | body | `string` | no | Display title of the appointment. |
| `appointment_note` | body | `string` | no | Accompanying notes for the appointment. |
| `status` | body | `string` | no | The status of the appointment. Valid statuses include `scheduled`, `confirmed`, `checked-in`, `in-room`, `cancelled`. Clinic custom statuses may also be used. |

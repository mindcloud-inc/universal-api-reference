# Create Appointment with Cerbo

Creates a new appointment in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Appointment](https://docs.cer.bo/#tag/Appointments/operation/createAppointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date_time` | body | `string` | yes | Starting datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `end_date_time` | body | `string` | yes | Ending datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `provider_ids[]` | body | `array<number>` | yes | An array of provider identifiers associated with this appointment. |
| `pt_id` | body | `number` | no | A patient identifier associated with this appointment. |
| `appointment_type` | body | `string` | yes | Valid appointment type `name`. |
| `title` | body | `string` | yes | Display title of the appointment. |
| `appointment_note` | body | `string` | yes | Accompanying notes for the appointment. |
| `status` | body | `string` | no | The status of the appointment. Valid statuses include `scheduled`, `confirmed`, `checked-in`, `in-room`, `cancelled`. Clinic custom statuses may also be used. |
| `telemedicine` | body | `boolean` | no | Flag for whether or not this is a telemedicine appointment. |

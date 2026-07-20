# Create Appointment with Rentman

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [Create Appointment](https://api.rentman.net/#operation/createAppointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Appointment name. |
| `start` | body | `date` | yes | Appointment start timestamp. |
| `end` | body | `date` | yes | Appointment end timestamp. |
| `location` | body | `string` | no | Appointment location. |
| `remark` | body | `string` | no | Appointment remark. |
| `is_public` | body | `boolean` | no | Whether the appointment is public. |
| `is_plannable` | body | `boolean` | no | Whether employees can be scheduled during this appointment. |

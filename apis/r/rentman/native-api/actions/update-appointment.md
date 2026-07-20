# Update Appointment with Rentman

## Endpoint

- **Method:** `PUT`
- **Path:** `/appointments/:id`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [Update Appointment](https://api.rentman.net/#operation/updateAppointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric ID of the appointment to update. |
| `start` | body | `date` | yes | Appointment start timestamp. |
| `end` | body | `date` | yes | Appointment end timestamp. |
| `name` | body | `string` | no | Appointment name. |
| `location` | body | `string` | no | Appointment location. |
| `remark` | body | `string` | no | Appointment remark. |
| `is_public` | body | `boolean` | no | Whether the appointment is public. |
| `is_plannable` | body | `boolean` | no | Whether employees can be scheduled during this appointment. |

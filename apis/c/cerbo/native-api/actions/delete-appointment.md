# Delete Appointment with Cerbo

Deletes an existing appointment from Cerbo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/appointments/:appointment_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Delete Appointment](https://docs.cer.bo/#tag/Appointments/operation/deleteAppointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointment_id` | path | `number` | yes | Appointment identifier. |

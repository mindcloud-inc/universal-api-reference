# Cancel Appointment with IntakeQ

Cancels an appointment in IntakeQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments/cancellation`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Cancel Appointment](https://support.intakeq.com/article/204-intakeq-appointments-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AppointmentId` | body | `string` | yes | The IntakeQ appointment ID. |

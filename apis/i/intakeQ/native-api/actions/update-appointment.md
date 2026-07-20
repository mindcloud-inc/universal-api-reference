# Update Appointment with IntakeQ

Updates an existing appointment in IntakeQ.

## Endpoint

- **Method:** `PUT`
- **Path:** `/appointments`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Update Appointment](https://support.intakeq.com/article/204-intakeq-appointments-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | yes | The IntakeQ appointment ID. |
| `UtcDateTime` | body | `string` | yes | Appointment start time as a Unix timestamp in milliseconds. |

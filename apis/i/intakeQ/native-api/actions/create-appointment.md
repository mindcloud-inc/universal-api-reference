# Create Appointment with IntakeQ

Creates a new appointment in IntakeQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/appointments`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Create Appointment](https://support.intakeq.com/article/204-intakeq-appointments-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PractitionerId` | body | `string` | yes | The IntakeQ practitioner ID. |
| `ClientId` | body | `string` | yes | The IntakeQ numeric client ID. |
| `ServiceId` | body | `string` | yes | The IntakeQ service ID. |
| `LocationId` | body | `string` | yes | The IntakeQ location ID. |
| `Status` | body | `string` | yes | Appointment status. |
| `UtcDateTime` | body | `string` | yes | Appointment start time as a Unix timestamp in milliseconds. |

# Create Appointment with mfr Field Service Management

Creates an appointment in mfr Field Service Management.

## Endpoint

- **Method:** `POST`
- **Path:** `Appointments`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Create Appointment](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Type` | body | `string` | yes | Appointment type. |
| `State` | body | `string` | yes | Appointment state. |
| `StartDateTime` | body | `date` | yes | Appointment start timestamp. |
| `EndDateTime` | body | `date` | yes | Appointment end timestamp. |
| `ContactId` | body | `string` | yes | Primary contact ID for the appointment. |

# Update Appointment with mfr Field Service Management

Updates an appointment in mfr Field Service Management.

## Endpoint

- **Method:** `PUT`
- **Path:** `Appointments({{id}}L)`
- **Base URL:** `https://portal.mobilefieldreport.com/odata`
- **Official documentation:** [Update Appointment](https://documenter.getpostman.com/view/6932380/2sB3dWsn6U)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `Id` | body | `string` | yes | Record ID in the request body. |
| `Type` | body | `string` | no | Updated appointment type. |
| `State` | body | `string` | no | Updated appointment state. |
| `StartDateTime` | body | `date` | no | Updated appointment start timestamp. |
| `EndDateTime` | body | `date` | no | Updated appointment end timestamp. |
| `ContactId` | body | `string` | no | Updated primary contact ID. |
| `ContactIds[]` | body | `array<string>` | no | Contact ID list for the appointment. |

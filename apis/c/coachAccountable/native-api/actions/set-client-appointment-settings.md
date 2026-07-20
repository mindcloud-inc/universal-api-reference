# Set Client Appointment Settings with CoachAccountable

Updates client appointment settings in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Set Client Appointment Settings](https://www.coachaccountable.com/APIDocs#Client.setAppointmentSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `selfScheduleRule` | body | `list` | no | Accepted values: `ABE`, `AUE`, `D`, `NA`. |
| `selfScheduleEmailConfirmations` | body | `boolean` | no | — |
| `attachICSFiles` | body | `boolean` | no | — |
| `allowedAppointmentTypeOption` | body | `list` | no | Accepted values: `A`, `S`. |
| `allowedAppointmentTypeIDList` | body | `string` | no | A comma-separated List of AppointmentTypeIDs (as returned by Appointment.getTypes) |

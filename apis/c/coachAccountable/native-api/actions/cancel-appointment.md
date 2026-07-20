# Cancel Appointment with CoachAccountable

Cancels an appointment in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Cancel Appointment](https://www.coachaccountable.com/APIDocs#Appointment.cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AppointmentID` | body | `number` | yes | — |
| `notifyClient` | body | `boolean` | no | Set to true to send a notification via email to the Client attendee of the Appointment. |
| `comment` | body | `string` | no | Optional comment from the Coach to be sent as part of the cancelation email to the Client. |

# Create Appointment with CoachAccountable

Creates an appointment in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Appointment](https://www.coachaccountable.com/APIDocs#Appointment.add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client whom the Appointment is with. |
| `AppointmentTypeID` | body | `number` | yes | The ID of the Appointment Type that the Appointment is to be of |
| `alternateLabel` | body | `string` | no | Optional alternate label for the appointment (overrides the Appointment Type's name) Maximum length: 100. |
| `location` | body | `string` | no | Optional alternate location for the appointment (overrides the Appointment Type's location) Maximum length: 100. |
| `description` | body | `string` | no | Optional alternate description for the appointment (overrides the Appointment Type's description) Maximum length: 100. |
| `dateOf` | body | `date` | yes | — |
| `timeOf` | body | `string` | yes | — |
| `timezoneOf` | body | `list` | no | Who's timezone the appointment date/time is in. Defaults to that of the Coach. Accepted values: `A`, `C`, `L`. |
| `sendNotification` | body | `boolean` | no | Send true if the Client should be sent a notification email immediately. |
| `notificationSubject` | body | `string` | no | Subject line of the notification email to be sent (if opted for). If not included, will use template setting. Maximum length: 200. |
| `notificationMessage` | body | `string` | no | Body of the notification email to be sent (if opted for). If not included, will use template setting. |
| `reminderSet` | body | `string` | no | A semi-colon-separated list of comma-separated triplets, each defining a reminder. In a triplet, the first value defines who to send it to ([C]oach or c[L]ient),the second value defines the send method ([E]mail or [T]ext), and the third value defines when to send the reminder, as minutes relative to the due date. Send "default" to set default reminders defined for the Appointment Type. |

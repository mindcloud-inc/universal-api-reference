# Add Authorized Attendee with Airmeet

Creates an authorized attendee in Airmeet.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet/{airmeetId}/attendee`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Add Authorized Attendee](https://help.airmeet.com/support/solutions/articles/82000909769-2-manage-registrations-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `attendance_type` | body | `string` | no | Required for hybrid events. Use IN-PERSON or VIRTUAL. |
| `email` | body | `string` | yes | The attendee email address. |
| `firstName` | body | `string` | yes | The attendee first name. |
| `lastName` | body | `string` | yes | The attendee last name. |
| `registerAttendee` | body | `boolean` | no | Set true to confirm the registration immediately instead of leaving it pending. |
| `sendEmailInvite` | body | `boolean` | no | Set false to skip sending the attendee email invite. |

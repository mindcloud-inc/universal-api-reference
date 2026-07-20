# Add Booking Attendee with Cal.com

Updates a booking in Cal.com by adding an attendee.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingUid/attendees`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Add Booking Attendee](https://cal.com/docs/api-reference/v2/bookings-attendees/add-an-attendee-to-a-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |
| `name` | body | `string` | yes | Attendee full name. |
| `timeZone` | body | `string` | yes | Attendee IANA time zone. |
| `email` | body | `string` | yes | Attendee email address. |

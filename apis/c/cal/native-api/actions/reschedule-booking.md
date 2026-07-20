# Reschedule Booking with Cal.com

Updates a booking in Cal.com by rescheduling it.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingUid/reschedule`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Reschedule Booking](https://cal.com/docs/api-reference/v2/bookings/reschedule-a-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |
| `start` | body | `string` | yes | New booking start time in ISO 8601 UTC format. |
| `reschedulingReason` | body | `string` | no | Reason text describing why the booking is being rescheduled. |
| `rescheduledBy` | body | `string` | no | Identifier for the actor who requested the reschedule. |
| `seatUid` | body | `string` | no | Seat booking UID when rescheduling a seat booking. |
| `emailVerificationCode` | body | `string` | no | Email verification code for protected event types. |

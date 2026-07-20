# Cancel Booking with Orufy Bookings

## Endpoint

- **Method:** `PATCH`
- **Path:** `/meet/cancel`
- **Base URL:** `https://bookings.orufy.com/api/v1/bookings`
- **Official documentation:** [Cancel Booking](https://orufy.com/support/bookings/bookingsevent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attendeeId` | body | `string` | yes | The attendee identifier returned by Get Booking Queue Status or Reschedule Booking. |
| `meetId` | body | `string` | yes | The meet identifier returned by Get Booking Queue Status or Reschedule Booking. |

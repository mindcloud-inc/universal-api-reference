# Reschedule Booking with Orufy Bookings

## Endpoint

- **Method:** `PATCH`
- **Path:** `/meet/reschedule`
- **Base URL:** `https://bookings.orufy.com/api/v1/bookings`
- **Official documentation:** [Reschedule Booking](https://orufy.com/support/bookings/bookingsevent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attendeeId` | body | `string` | yes | The attendee identifier returned by Get Booking Queue Status or Reschedule Booking. |
| `meetId` | body | `string` | yes | The meet identifier returned by Get Booking Queue Status or Reschedule Booking. |
| `timezone` | body | `string` | yes | An IANA timezone, for example `America/Sao_Paulo`. |
| `time[]` | body | `array<object>` | yes | An array of time objects. Each item must include a `time` ISO datetime value. |

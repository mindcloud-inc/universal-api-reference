# Cancel Booking with Cal.com

Updates a booking in Cal.com by canceling it.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingUid/cancel`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Cancel Booking](https://cal.com/docs/api-reference/v2/bookings/cancel-a-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |
| `cancellationReason` | body | `string` | no | Reason text to include when canceling the booking. |
| `cancelSubsequentBookings` | body | `boolean` | no | Whether to cancel future bookings in the recurring series. |
| `seatUid` | body | `string` | no | Seat booking UID when canceling a seat booking. |

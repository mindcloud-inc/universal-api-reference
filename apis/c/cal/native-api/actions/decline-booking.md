# Decline Booking with Cal.com

Updates a booking in Cal.com by declining it.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingUid/decline`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Decline Booking](https://cal.com/docs/api-reference/v2/bookings/decline-a-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |

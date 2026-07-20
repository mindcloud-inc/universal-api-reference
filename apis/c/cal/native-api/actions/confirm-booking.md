# Confirm Booking with Cal.com

Updates a booking in Cal.com by confirming it.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings/:bookingUid/confirm`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Confirm Booking](https://cal.com/docs/api-reference/v2/bookings/confirm-a-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingUid` | path | `list` | yes | Booking identifier from Cal.com path parameter. |

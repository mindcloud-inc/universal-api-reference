# List Booking Tickets with Understory

Retrieves tickets for a booking in Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bookings/{{bookingId}}/tickets`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Booking Tickets](https://developer.understory.io/apis/booking/gettickets.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | path | `string` | yes | The unique identifier of the booking. |

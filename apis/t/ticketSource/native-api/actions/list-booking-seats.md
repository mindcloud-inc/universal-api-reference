# List Booking Seats with TicketSource

Retrieves seats for a booking from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/bookings/{BookingId}/seats`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Booking Seats](https://www.ticketsource.io/working-with-bookings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BookingId` | path | `string` | yes | The unique identifier for a Booking record |

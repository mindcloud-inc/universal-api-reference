# List Date Bookings with TicketSource

Retrieves bookings for a date from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/dates/{DateId}/bookings`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Date Bookings](https://www.ticketsource.io/working-with-bookings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DateId` | path | `string` | yes | The unique identifier for a Date record |

# List Customer Bookings with TicketSource

Retrieves bookings for a customer from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/{CustomerId}/bookings`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Customer Bookings](https://www.ticketsource.io/working-with-bookings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerId` | path | `string` | yes | The unique identifier for a Customer record |

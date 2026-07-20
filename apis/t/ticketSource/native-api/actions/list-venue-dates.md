# List Venue Dates with TicketSource

Retrieves dates for a venue from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/venues/{VenueId}/dates`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Venue Dates](https://www.ticketsource.io/working-with-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `VenueId` | path | `string` | yes | The unique identifier for a Venue record |

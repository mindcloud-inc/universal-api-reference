# List Event Dates with TicketSource

Retrieves dates for an event from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/{EventId}/dates`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Event Dates](https://www.ticketsource.io/working-with-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EventId` | path | `string` | yes | The unique identifier for an Event record |

# List Event Venues with TicketSource

Retrieves venues for an event from TicketSource.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/{EventId}/venues`
- **Base URL:** `https://api.ticketsource.io`
- **Official documentation:** [List Event Venues](https://www.ticketsource.io/working-with-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EventId` | path | `string` | yes | The unique identifier for an Event record |

# Get Ticket History with Request Tracker (RT)

Retrieves a ticket's history from Request Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `ticket/:ticketId/history`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Get Ticket History](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Transactions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The numeric RT ticket ID. |

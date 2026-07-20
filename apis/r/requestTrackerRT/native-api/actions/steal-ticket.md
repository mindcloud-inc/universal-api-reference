# Steal Ticket with Request Tracker (RT)

Reassigns a ticket to yourself in Request Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `ticket/:ticketId/steal`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Steal Ticket](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `string` | yes | The numeric RT ticket ID. |

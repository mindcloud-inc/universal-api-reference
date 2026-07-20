# Correspond on Ticket with Request Tracker (RT)

Adds a reply to a ticket in Request Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `ticket/:ticketId/correspond`
- **Base URL:** `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`
- **Official documentation:** [Correspond on Ticket](https://docs.bestpractical.com/rt/6.0.2/RT/REST2.html#Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Content` | body | `string` | yes | Reply body to add to the ticket. |
| `ContentType` | body | `string` | yes | Content type for the reply body. |
| `Subject` | body | `string` | no | Optional subject for the correspondence. |
| `ticketId` | path | `string` | yes | The numeric RT ticket ID. |

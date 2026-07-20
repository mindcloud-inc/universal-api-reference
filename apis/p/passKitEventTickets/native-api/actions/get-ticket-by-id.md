# Get Ticket By Id with PassKit Event Tickets

Retrieves a ticket by ID from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/ticket/id/:id`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Ticket By Id](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PassKit ticket id to retrieve. |

# Get Ticket By Ticket Number with PassKit Event Tickets

Retrieves a ticket by ticket number from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/ticket/ticketNumber`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Ticket By Ticket Number](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketByTicketNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | query | `string` | no | Filter the ticket lookup by production id. |
| `productionUid` | query | `string` | no | Filter the ticket lookup by production uid. |
| `ticketNumber` | query | `string` | no | Ticket number to look up. |

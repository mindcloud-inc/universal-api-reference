# Get Ticket Type By Uid with PassKit Event Tickets

Retrieves a ticket type by user-defined ID from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/ticketType/uid/:productionId/:uid`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Ticket Type By Uid](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketTypeByUserDefinedId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | path | `string` | yes | PassKit production id for the ticket type lookup. |
| `uid` | path | `string` | yes | Provider uid for the ticket type lookup. |

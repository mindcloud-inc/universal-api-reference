# List Ticket Types with PassKit Event Tickets

Retrieves ticket types from PassKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventTickets/ticketTypes/:productionId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Ticket Types](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listTicketTypes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | path | `string` | yes | PassKit production id whose ticket types you want to list. |

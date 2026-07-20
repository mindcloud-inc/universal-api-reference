# List Tickets with PassKit Event Tickets

Retrieves tickets for a production from PassKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventTickets/tickets/list`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Tickets](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listTickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | body | `string` | no | PassKit production id filter for the ticket list request. |
| `productionUid` | body | `string` | no | PassKit production uid filter for the ticket list request. |

# List Tickets By Order Number with PassKit Event Tickets

Retrieves tickets by order number from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/tickets/orderNumber`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Tickets By Order Number](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getTicketsByOrderNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderNumber` | query | `string` | no | Order number whose tickets you want to list. |
| `productionId` | query | `string` | no | Filter order-number ticket lookup by production id. |
| `productionUid` | query | `string` | no | Filter order-number ticket lookup by production uid. |

# Count Tickets with PassKit Event Tickets

Retrieves a filtered ticket count from PassKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventTickets/tickets/count`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Count Tickets](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_countTickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | body | `string` | no | PassKit production id filter for the ticket count request. |
| `productionUid` | body | `string` | no | PassKit production uid filter for the ticket count request. |

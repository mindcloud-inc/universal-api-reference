# List Events with PassKit Event Tickets

Retrieves events for a production from PassKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventTickets/events/list`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Events](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_listEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | body | `string` | no | PassKit production id filter for the event list request. |
| `productionUid` | body | `string` | no | PassKit production uid filter for the event list request. |

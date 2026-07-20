# Get Event with PassKit Event Tickets

Retrieves event details from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/event/id/:id`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Event](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getEventById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PassKit event id to retrieve. |

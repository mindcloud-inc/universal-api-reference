# Get Venue with PassKit Event Tickets

Retrieves venue details from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/venue/:id`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Venue](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getVenueById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PassKit venue id to retrieve. |

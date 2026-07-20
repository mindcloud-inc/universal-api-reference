# Get Production with PassKit Event Tickets

Retrieves production details from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/production/:id`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Production](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getProduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PassKit production id to retrieve. |

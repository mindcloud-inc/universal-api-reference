# List Event Tickets with Eventzilla

Retrieves tickets for an event from Eventzilla.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventid/tickets`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [List Event Tickets](https://developer.eventzilla.net/docs/#ev_tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventid` | path | `number` | yes | The Eventzilla event identifier. |

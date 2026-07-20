# Get Event Details with PassKit Event Tickets

Retrieves an event by start date and venue from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/event/details`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Event Details](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getEventByStartDateAndVenue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productionId` | query | `string` | no | Filter event details by production id. |
| `productionUid` | query | `string` | no | Filter event details by production uid. |
| `scheduledStartDate` | query | `string` | no | Filter event details by scheduled start date. |
| `venueId` | query | `string` | no | Filter event details by venue id. |
| `venueUid` | query | `string` | no | Filter event details by venue uid. |

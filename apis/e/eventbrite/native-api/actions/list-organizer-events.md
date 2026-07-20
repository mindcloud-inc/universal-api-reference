# List Organizer Events with Eventbrite

Retrieves organizer events from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizers/:organizerId/events/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Organizer Events](https://www.eventbrite.com/platform/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizerId` | path | `string` | yes | Organizer identifier. |

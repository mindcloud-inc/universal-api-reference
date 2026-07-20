# Update Organizer with Eventbrite

Updates an existing organizer in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizers/:organizerId/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Update Organizer](https://www.eventbrite.com/platform/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizer.name` | body | `string` | yes | Updated organizer name. |
| `organizerId` | path | `string` | yes | Organizer identifier. |

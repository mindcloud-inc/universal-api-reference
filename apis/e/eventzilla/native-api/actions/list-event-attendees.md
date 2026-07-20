# List Event Attendees with Eventzilla

Retrieves attendees for an event from Eventzilla.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventid/attendees`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [List Event Attendees](https://developer.eventzilla.net/docs/#ev_attendee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventid` | path | `number` | yes | The Eventzilla event identifier. |

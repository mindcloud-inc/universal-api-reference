# Search RSVP attendees with AddEvent

## Endpoint

- **Method:** `GET`
- **Path:** `/rsvps`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Search RSVP attendees](https://docs.addevent.com/reference/search-rsvp-attendees)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendar_ids[]` | query | `array<string>` | no | Limit results to specific calendars. Send multiple values as a string separated by `,`. |
| `event_ids[]` | query | `array<string>` | no | Limit results to specific events. Send multiple values as a string separated by `,`. |
| `attending[]` | query | `array<string>` | no | Filter RSVP attendees by response status. Send multiple values as a string separated by `,`. |

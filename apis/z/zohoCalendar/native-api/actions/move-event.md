# Move Event with Zoho Calendar

Moves an event to another calendar in Zoho Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `/calendars/:calendaruid/events/:eventuid`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Move Event](https://www.zoho.com/calendar/help/api/move-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Source calendar unique identifier. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `destinationcaluid` | query | `string` | yes | Destination calendar unique identifier. |
| `eventdata` | query | `object` | no | Optional event payload object to apply while moving the event. |

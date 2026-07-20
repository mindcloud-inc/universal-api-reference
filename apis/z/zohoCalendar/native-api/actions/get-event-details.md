# Get Event Details with Zoho Calendar

Retrieves details for an event in Zoho Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars/:calendaruid/events/:eventuid`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Get Event Details](https://www.zoho.com/calendar/help/api/get-event-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier for the event. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `recurrenceid` | query | `string` | no | Specific recurrence instance identifier. |

# Get Event By Instance with Zoho Calendar

Retrieves instances of a recurring event in Zoho Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars/:calendaruid/events/:eventuid/byinstance`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Get Event By Instance](https://www.zoho.com/calendar/help/api/get-event-by-instance.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `range` | query | `object` | yes | Date range object for the event instance lookup. |

# Create Event with Zoho Calendar

Creates a new event in Zoho Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `/calendars/:calendaruid/events`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Create Event](https://www.zoho.com/calendar/help/api/post-create-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `eventdata` | query | `object` | yes | Event payload object describing the new event. |

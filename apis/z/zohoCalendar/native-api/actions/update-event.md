# Update Event with Zoho Calendar

Updates an existing event in Zoho Calendar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendars/:calendaruid/events/:eventuid`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Update Event](https://www.zoho.com/calendar/help/api/put-update-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `eventdata` | query | `object` | yes | Event payload object with the fields to update. |

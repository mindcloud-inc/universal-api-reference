# Partial Update Event with Zoho Calendar

Updates specific event fields in Zoho Calendar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/calendars/:calendaruid/events/:eventuid`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Partial Update Event](https://www.zoho.com/calendar/help/api/patch-partial-update-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `eventdata` | query | `object` | yes | Event payload object with the partial fields to update. |

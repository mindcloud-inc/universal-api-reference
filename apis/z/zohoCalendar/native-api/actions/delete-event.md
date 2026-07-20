# Delete Event with Zoho Calendar

Deletes an existing event from Zoho Calendar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/calendars/:calendaruid/events/:eventuid`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Delete Event](https://www.zoho.com/calendar/help/api/delete-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `eventdata` | query | `object` | no | Zoho's live delete endpoint requires `eventData.uid` and `eventData.etag` from a prior event read response, even for standard single-event deletes. |

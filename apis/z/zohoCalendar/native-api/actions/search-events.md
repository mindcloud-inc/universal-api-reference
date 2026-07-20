# Search Events with Zoho Calendar

Finds events in a Zoho Calendar calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars/:calendaruid/search`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Search Events](https://www.zoho.com/calendar/help/api/get-event-through-search.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier to search within. |
| `searchtext` | query | `string` | yes | Text to search for in event titles. |
| `start` | query | `string` | yes | Search start datetime in yyyyMMdd'T'HHmmss'Z' format. |
| `end` | query | `string` | yes | Search end datetime in yyyyMMdd'T'HHmmss'Z' format. |

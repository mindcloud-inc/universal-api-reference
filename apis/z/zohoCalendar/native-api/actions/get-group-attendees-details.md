# Get Group Attendees Details with Zoho Calendar

Retrieves group attendee details for an event in Zoho Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendars/:calendaruid/events/:eventuid/groupattendeestatus`
- **Base URL:** `https://calendar.zoho.com/api/v1`
- **Official documentation:** [Get Group Attendees Details](https://www.zoho.com/calendar/help/api/get-group-attendees-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calendaruid` | path | `string` | yes | Calendar unique identifier. |
| `eventuid` | path | `string` | yes | Event unique identifier. |
| `groupId` | query | `number` | yes | Numeric group identifier for the attendee status lookup. |

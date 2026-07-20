# List Calendar View with Microsoft 365 Calendar

Retrieves events from Microsoft 365 Calendar for a time range.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/calendarView`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Calendar View](https://learn.microsoft.com/en-us/graph/api/user-list-calendarview?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDateTime` | query | `string` | yes | Start of the calendar view window in ISO 8601 format. |
| `endDateTime` | query | `string` | yes | End of the calendar view window in ISO 8601 format. |
| `$top` | query | `number` | no | Number of events to return in the requested calendar window. |

# Delete Event with Google Calendar

Deletes an existing event from Google Calendar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `calendars/:calendar/events/:eventId`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Delete Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | yes |
| `eventId` | path | `string` | yes |
| `sendUpdates` | query | `list` | no |

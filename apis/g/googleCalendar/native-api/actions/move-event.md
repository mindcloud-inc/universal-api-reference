# Move Event with Google Calendar

Moves an event to another calendar in Google Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `calendars/:calendar/events/:eventId/move`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Move Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/move)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `eventId` | path | `string` | no |
| `destination` | query | `list` | no |

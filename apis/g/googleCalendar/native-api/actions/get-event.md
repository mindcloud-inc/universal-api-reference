# Get Event with Google Calendar

Retrieves an event from Google Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `calendars/:calendar/events/:eventId`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Get Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `eventId` | path | `string` | no |

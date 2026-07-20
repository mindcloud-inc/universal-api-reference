# Quick Add Event with Google Calendar

Creates an event from text in Google Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `calendars/:calendar/events/quickAdd`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Quick Add Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/quickAdd)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `text` | query | `string` | no |

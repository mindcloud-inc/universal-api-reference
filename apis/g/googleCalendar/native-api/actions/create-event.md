# Create Event with Google Calendar

Creates a new event in Google Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `calendars/:calendar/events`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Create Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/insert)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attendees[].email` | body | `string` | no |
| `calendar` | path | `list` | yes |
| `summary` | body | `string` | no |
| `location` | body | `string` | no |
| `description` | body | `string` | no |
| `start` | body | `date` | no |
| `end` | body | `date` | no |
| `attendees[]` | body | `array` | no |

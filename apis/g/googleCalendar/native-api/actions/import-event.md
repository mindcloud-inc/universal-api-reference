# Import Event with Google Calendar

Imports a private event copy into Google Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `calendars/:calendar/events/import`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Import Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/import)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `iCalUID` | body | `string` | no |
| `summary` | body | `string` | no |
| `start.dateTime` | body | `date` | no |
| `end.dateTime` | body | `date` | no |

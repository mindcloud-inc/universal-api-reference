# Update Event with Google Calendar

Updates an existing event in Google Calendar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `calendars/:calendar/events/:eventId`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Update Event](https://developers.google.com/workspace/calendar/api/v3/reference/events/patch)

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
| `eventId` | path | `string` | yes |

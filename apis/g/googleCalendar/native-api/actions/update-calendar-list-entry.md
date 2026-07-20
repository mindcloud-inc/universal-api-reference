# Update Calendar List Entry with Google Calendar

Updates an existing calendar list entry in Google Calendar.

## Endpoint

- **Method:** `PUT`
- **Path:** `users/me/calendarList/:calendar`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Update Calendar List Entry](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `summaryOverride` | body | `string` | no |

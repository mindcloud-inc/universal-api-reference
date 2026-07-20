# Patch Calendar List Entry with Google Calendar

Updates a calendar list entry in Google Calendar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `users/me/calendarList/:calendar`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Patch Calendar List Entry](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `summaryOverride` | body | `string` | no |

# List Calendars with Google Calendar

Retrieves calendar list entries from Google Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `users/me/calendarList`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [List Calendars](https://developers.google.com/workspace/calendar/api/v3/reference/calendarList/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minAccessRole` | query | `list` | no | — |
| `showHidden` | query | `boolean` | no | Format: `toggle`. |
| `showDeleted` | query | `boolean` | no | Format: `toggle`. |

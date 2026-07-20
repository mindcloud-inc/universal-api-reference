# Create Event with Microsoft 365 Calendar

Creates a new event in Microsoft 365 Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/events`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Event](https://learn.microsoft.com/en-us/graph/api/user-post-events?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | The calendar event subject. |
| `start.dateTime` | body | `string` | yes | Event start date and time in ISO format. Use UTC values such as 2026-03-19T15:00:00. |
| `end.dateTime` | body | `string` | yes | Event end date and time in ISO format. Use UTC values such as 2026-03-19T15:30:00. |
| `location.displayName` | body | `string` | no | Optional event location display name. |

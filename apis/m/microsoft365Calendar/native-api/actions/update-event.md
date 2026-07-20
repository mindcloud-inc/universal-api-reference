# Update Event with Microsoft 365 Calendar

Updates an existing event in Microsoft 365 Calendar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/events/{{eventId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Update Event](https://learn.microsoft.com/en-us/graph/api/event-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The ID of the Outlook event to update. |
| `subject` | body | `string` | no | Updated subject for the Outlook event. |
| `start.dateTime` | body | `string` | no | Optional updated event start date and time. |
| `end.dateTime` | body | `string` | no | Optional updated event end date and time. |
| `start.timeZone` | body | `string` | no | Optional updated event start time zone. Provide this when changing the start date/time. |
| `end.timeZone` | body | `string` | no | Optional updated event end time zone. Provide this when changing the end date/time. |
| `location.displayName` | body | `string` | no | Optional updated event location display name. |

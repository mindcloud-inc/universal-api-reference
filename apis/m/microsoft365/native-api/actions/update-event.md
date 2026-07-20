# Update Event with Microsoft 365

Updates an event in Microsoft 365.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/events/{{eventId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Update Event](https://learn.microsoft.com/en-us/graph/api/event-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The ID of the Outlook event to update. |
| `subject` | body | `string` | no | Updated subject for the Outlook event. |
| `start.dateTime` | body | `string` | no | Updated event start date and time in ISO format. Provide this with an updated end date and time. |
| `end.dateTime` | body | `string` | no | Updated event end date and time in ISO format. Provide this with an updated start date and time. |
| `start.timeZone` | body | `string` | no | Time zone to use with the updated event start date and time. |
| `end.timeZone` | body | `string` | no | Time zone to use with the updated event end date and time. |
| `location.displayName` | body | `string` | no | Updated display name for the event location. |

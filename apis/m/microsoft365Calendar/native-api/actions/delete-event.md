# Delete Event with Microsoft 365 Calendar

Deletes an existing event from Microsoft 365 Calendar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/me/events/{{eventId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete Event](https://learn.microsoft.com/en-us/graph/api/event-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The ID of the Outlook event to delete. |

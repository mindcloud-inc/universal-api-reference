# Get Event with Microsoft 365 Calendar

Retrieves an event from Microsoft 365 Calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/events/{{eventId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Event](https://learn.microsoft.com/en-us/graph/api/event-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The ID of the Outlook event. |

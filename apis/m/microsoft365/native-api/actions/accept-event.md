# Accept Event with Microsoft 365

Accepts an event in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/events/:eventId/accept`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Accept Event](https://learn.microsoft.com/en-us/graph/api/event-accept?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The ID of the Outlook event to accept. |
| `comment` | body | `string` | no | — |

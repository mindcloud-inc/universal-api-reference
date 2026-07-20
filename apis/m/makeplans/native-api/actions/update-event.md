# Update Event with Makeplans

Updates an existing event in Makeplans.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Event](https://developer.makeplans.com/endpoints/events/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event.capacity` | body | `number` | no | Event capacity. |
| `event.title` | body | `string` | no | Event title. |
| `eventId` | path | `number` | yes | The Makeplans event ID. |

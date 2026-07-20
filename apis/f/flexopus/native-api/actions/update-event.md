# Update Event with Flexopus

Updates an existing event in Flexopus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:id`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Update Event](https://flexopus.com/api/docs/#endpoints-PUTapi-v1-events--id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the event. |
| `from_time` | body | `date` | no | When the event will start. |
| `from_timezone` | body | `string` | no | Display timezone of the event start time. |
| `to_time` | body | `date` | no | When the event will end. |
| `to_timezone` | body | `string` | no | Display timezone of the event end time. |
| `classification` | body | `list<number>` | no | Access classification for the event. Accepted values: `0`, `1`, `2`, `3`. |
| `name` | body | `string` | no | Event name. |
| `description` | body | `string` | no | Event markdown description. |
| `attendees[]` | body | `array<object>` | no | List of attendees for the event as a JSON array of attendee objects. |

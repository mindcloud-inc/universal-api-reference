# Create Event with Flexopus

Creates a new event in Flexopus.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Create Event](https://flexopus.com/api/docs/#endpoints-POSTapi-v1-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_time` | body | `date` | no | When the event will start. |
| `from_timezone` | body | `string` | no | Display timezone of the event start time. |
| `to_time` | body | `date` | yes | When the event will end. |
| `to_timezone` | body | `string` | no | Display timezone of the event end time. |
| `classification` | body | `list<number>` | no | Access classification for the event. Accepted values: `0`, `1`, `2`, `3`. |
| `name` | body | `string` | yes | Event name. |
| `description` | body | `string` | no | Event markdown description. |
| `organizer_user_id` | body | `number` | yes | ID of the event organizer user. |
| `attendees[]` | body | `array<object>` | no | List of attendees for the event as a JSON array of attendee objects. |

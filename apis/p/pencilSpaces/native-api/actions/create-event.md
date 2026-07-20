# Create Event with Pencil Spaces

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://apis.pencilapp.com/public/api`
- **Official documentation:** [Create Event](https://api.pencilspaces.com/guide/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description of the event. |
| `end` | body | `string` | no | RFC3339 end timestamp for the event. |
| `organizers[]` | body | `array<object>` | no | Organizer list for the event. |
| `organizers[].userId` | body | `string` | no | Organizer userId. |
| `spaceId` | body | `string` | no | The Pencil spaceId associated with the event. |
| `start` | body | `string` | no | RFC3339 start timestamp for the event. |
| `title` | body | `string` | no | Title of the event. |

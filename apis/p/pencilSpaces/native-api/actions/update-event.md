# Update Event with Pencil Spaces

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId`
- **Base URL:** `https://apis.pencilapp.com/public/api`
- **Official documentation:** [Update Event](https://api.pencilspaces.com/guide/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated description of the event. |
| `end` | body | `string` | no | Updated RFC3339 end timestamp for the event. |
| `eventId` | path | `string` | yes | The Pencil eventId of the event to update. |
| `organizers[]` | body | `array<object>` | no | Organizer list for the event. |
| `organizers[].userId` | body | `string` | no | Organizer userId. |
| `spaceId` | body | `string` | no | Updated Pencil spaceId associated with the event. |
| `start` | body | `string` | no | Updated RFC3339 start timestamp for the event. |
| `title` | body | `string` | no | Updated title of the event. |

# Update Calendar Event with Instructure

Updates an existing calendar event in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/calendar_events/:event_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Calendar Event](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Canvas calendar event ID. |
| `start_at` | body | `string` | no | The calendar event start datetime in ISO-8601 format. |
| `title` | body | `string` | no | The updated calendar event title. |

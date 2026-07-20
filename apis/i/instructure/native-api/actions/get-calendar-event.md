# Get Calendar Event with Instructure

Retrieves a calendar event from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/calendar_events/:event_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Calendar Event](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Canvas calendar event ID. |

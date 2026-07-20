# Delete Calendar Event with Instructure

Deletes a calendar event from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/calendar_events/:event_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Delete Calendar Event](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Canvas calendar event ID. |

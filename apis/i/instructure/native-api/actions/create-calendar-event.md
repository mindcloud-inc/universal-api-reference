# Create Calendar Event with Instructure

Creates a new calendar event in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/calendar_events`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Calendar Event](https://developerdocs.instructure.com/services/canvas/resources/calendar_events#method.calendar_events_api.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context_code` | body | `string` | yes | The Canvas context code such as course_123 or user_247427066. |
| `end_at` | body | `string` | yes | The calendar event end datetime in ISO-8601 format. |
| `start_at` | body | `string` | yes | The calendar event start datetime in ISO-8601 format. |
| `title` | body | `string` | yes | The calendar event title. |

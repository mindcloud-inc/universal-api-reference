# Update event with AddEvent

## Endpoint

- **Method:** `PATCH`
- **Path:** `/events/:event_id`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Update event](https://docs.addevent.com/reference/update-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Unique identifier for the event. |
| `title` | body | `string` | no | — |
| `calendar_id` | body | `string` | no | — |
| `datetime_start` | body | `string` | no | — |
| `datetime_end` | body | `string` | no | — |
| `all_day_event` | body | `boolean` | no | Whether the event should be treated as an all-day event. |
| `timezone` | body | `string` | no | — |
| `recurring_rule` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `internal_name` | body | `string` | no | — |
| `location` | body | `string` | no | — |
| `location_id` | body | `number` | no | — |
| `organizer_name` | body | `string` | no | — |
| `organizer_email` | body | `string` | no | — |
| `reminder` | body | `number` | no | Minutes before start time to send a reminder. |
| `color` | body | `number` | no | Palette color value for the event. |
| `free_busy` | body | `string` | no | Whether the event appears as free, busy, or uses the default. |
| `landing_page_template_id` | body | `string` | no | Custom event landing page template ID or default. |
| `rsvp_enabled` | body | `boolean` | no | Whether attendees must RSVP before adding the event. |
| `rsvp_form_id` | body | `string` | no | Custom RSVP form ID or default. |
| `custom_data` | body | `object` | no | — |

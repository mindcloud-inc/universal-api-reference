# Create event with AddEvent

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Create event](https://docs.addevent.com/reference/create-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | The event title. |
| `calendar_id` | body | `string` | no | Calendar ID to associate with the event. |
| `datetime_start` | body | `string` | no | Start date and time for the event. |
| `datetime_end` | body | `string` | no | End date and time for the event. |
| `all_day_event` | body | `boolean` | no | Whether the event should be treated as an all-day event. |
| `timezone` | body | `string` | no | Timezone for the event. |
| `recurring_rule` | body | `string` | no | iCalendar RRULE value for recurring events. |
| `description` | body | `string` | no | Event description shown to attendees. |
| `internal_name` | body | `string` | no | Internal-only event name. |
| `location` | body | `string` | no | Address or URL for the event location. |
| `location_id` | body | `number` | no | Saved location ID to associate with the event. |
| `organizer_name` | body | `string` | no | Organizer name displayed on the event. |
| `organizer_email` | body | `string` | no | Organizer email displayed on the event. |
| `reminder` | body | `number` | no | Minutes before start time to send a reminder. |
| `color` | body | `number` | no | Palette color value for the event. |
| `free_busy` | body | `string` | no | Whether the event appears as free, busy, or uses the default. |
| `landing_page_template_id` | body | `string` | no | Custom event landing page template ID or default. |
| `rsvp_enabled` | body | `boolean` | no | Whether attendees must RSVP before adding the event. |
| `rsvp_form_id` | body | `string` | no | Custom RSVP form ID or default. |
| `custom_data` | body | `object` | no | Structured key-value data attached to the event. |

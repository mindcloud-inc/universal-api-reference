# Create Event with CalendarLink

Creates a new event in a CalendarLink organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/:organisation/event`
- **Base URL:** `https://my.calendarlink.com/api/v1`
- **Official documentation:** [Create Event](https://api.swaggerhub.com/apis/Calendarlink/calendarlink/1.0.3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection_id` | body | `list<string>` | yes | Collection ID that owns the event. |
| `organisation` | path | `string` | yes | CalendarLink organization ID. |
| `rsvp.enabled` | body | `boolean` | no | Whether RSVP is enabled for the event. |
| `rsvp.settings.max_attendees` | body | `number` | no | Maximum RSVP attendee count. |
| `rsvp.description` | body | `string` | no | RSVP description shown to invitees. |
| `rsvp.settings.notification` | body | `string` | no | RSVP notification mode. |
| `title` | body | `string` | yes | Event title. |
| `rsvp.deadline` | body | `string` | no | RSVP deadline timestamp. |
| `rsvp.settings.notification_email` | body | `string` | no | Email used for RSVP notifications. |
| `start` | body | `string` | yes | Event start datetime in `YYYY-MM-DD HH:MM:SS` format. |
| `end` | body | `string` | yes | Event end datetime in `YYYY-MM-DD HH:MM:SS` format. |
| `rsvp.settings.phone_enabled` | body | `boolean` | no | Whether phone input is enabled for RSVP. |
| `rsvp.settings.description_enabled` | body | `boolean` | no | Whether the RSVP description field is enabled. |
| `timezone` | body | `string` | no | Timezone identifier for the event. |
| `date_format` | body | `string` | no | Date format preference. |
| `rsvp.settings.description_label` | body | `string` | no | Label shown for the RSVP description field. |
| `description` | body | `string` | no | Event description. |
| `location` | body | `string` | no | Event location text. |
| `location_url` | body | `string` | no | Event location URL. |

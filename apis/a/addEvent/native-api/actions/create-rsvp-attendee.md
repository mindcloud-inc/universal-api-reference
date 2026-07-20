# Create RSVP attendee with AddEvent

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:event_id/rsvps`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Create RSVP attendee](https://docs.addevent.com/reference/create-rsvp-attendee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Unique identifier for the event. |
| `email` | body | `string` | no | Email address for the RSVP attendee. |
| `attending` | body | `string` | no | RSVP response status. |
| `notify` | body | `string` | no | Optional. Leave blank unless you want AddEvent notification emails; when used, set this to active. |
| `rsvp_form_data` | body | `object` | no | For the default RSVP form, include `{ "name": "Attendee Name" }`. Custom RSVP forms may require additional keys. |

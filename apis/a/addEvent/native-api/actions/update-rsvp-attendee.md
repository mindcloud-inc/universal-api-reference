# Update RSVP attendee with AddEvent

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rsvps/:attendee_id`
- **Base URL:** `https://api.addevent.com/calevent/v2`
- **Official documentation:** [Update RSVP attendee](https://docs.addevent.com/reference/update-rsvp-attendee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attendee_id` | path | `string` | yes | Unique identifier for the RSVP attendee. |
| `email` | body | `string` | no | — |
| `attending` | body | `string` | no | RSVP response status. |
| `notify` | body | `string` | no | Optional. Leave blank unless you want AddEvent notification emails; when used, set this to active. |
| `rsvp_form_data` | body | `object` | no | For the default RSVP form, include `{ "name": "Attendee Name" }`. Custom RSVP forms may require additional keys. |

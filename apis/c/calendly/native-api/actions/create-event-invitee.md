# Create Event Invitee with Calendly

Creates an event invitee in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitees`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Create Event Invitee](https://developer.calendly.com/api-docs/p3ghrxrwbl8kqe-create-event-invitee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | body | `string` | yes | Event type URI. |
| `start_time` | body | `date` | yes | Invitee start time (ISO-8601). |
| `end_time` | body | `date` | yes | Invitee end time (ISO-8601). |
| `invitee` | body | `object` | yes | — |
| `invitee.name` | body | `string` | yes | Invitee full name. |
| `invitee.email` | body | `string` | yes | Invitee email. |
| `invitee.timezone` | body | `string` | no | Invitee timezone. |
| `location` | body | `object` | yes | — |
| `location.kind` | body | `string` | yes | Location kind configured on the event type (for example google_conference). |

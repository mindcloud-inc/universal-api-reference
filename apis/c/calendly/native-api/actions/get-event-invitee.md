# Get Event Invitee with Calendly

Retrieves an invitee for a Calendly event.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduled_events/:event_uuid/invitees/:invitee_uuid`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Get Event Invitee](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_uuid` | path | `string` | yes | Scheduled event UUID. |
| `invitee_uuid` | path | `string` | yes | Invitee UUID. |

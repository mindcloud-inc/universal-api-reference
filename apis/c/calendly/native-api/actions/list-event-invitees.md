# List Event Invitees with Calendly

Retrieves invitees for a Calendly event.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduled_events/:event_uuid/invitees`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Event Invitees](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_uuid` | path | `string` | yes | Scheduled event UUID. |
| `status` | query | `list` | no | Invitee status filter. Accepted values: `active`, `canceled`. |
| `email` | query | `string` | no | Filter invitees by email address. |
| `sort` | query | `list` | no | Sort order for event invitees. Accepted values: `created_at:asc`, `created_at:desc`. |

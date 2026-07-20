# Get Scheduled Event with Calendly

Retrieves a scheduled event from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduled_events/:event_uuid`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Get Scheduled Event](https://developer.calendly.com/update-your-system-with-data-from-scheduled-events-admins-only)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_uuid` | path | `string` | yes | Scheduled event UUID. |

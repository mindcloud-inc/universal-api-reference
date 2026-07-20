# Create Single-Use Scheduling Link with Calendly

Creates a single-use scheduling link in Calendly.

## Endpoint

- **Method:** `POST`
- **Path:** `/scheduling_links`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [Create Single-Use Scheduling Link](https://developer.calendly.com/api-docs/4b8195084e287-create-single-use-scheduling-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | body | `string` | yes | Owner URI (event type or user). |
| `owner_type` | body | `string` | yes | Owner type: EventType or User. |
| `max_event_count` | body | `number` | no | Maximum times this link can be used. |
| `expires_at` | body | `date` | no | Scheduling link expiration time (ISO-8601). |

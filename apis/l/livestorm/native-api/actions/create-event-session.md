# Create Event Session with Livestorm

Creates a new session for an event in Livestorm.

## Endpoint

- **Method:** `POST`
- **Path:** `events/:id/sessions`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Create Event Session](https://developers.livestorm.co/reference/post_events-id-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `data.attributes.estimated_started_at` | body | `date` | no | — |
| `data.attributes.timezone` | body | `string` | no | — |
| `data.attributes.name` | body | `string` | no | — |
| `data.relationships.people[]` | body | `array<object>` | no | — |
| `data.relationships.people[].data.type` | body | `string` | no | — |
| `data.relationships.people[].data.id` | body | `string` | no | — |
| `data.relationships.people[].data.role` | body | `string` | no | — |

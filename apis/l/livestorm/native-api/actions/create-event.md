# Create Event with Livestorm

Creates a new event in Livestorm.

## Endpoint

- **Method:** `POST`
- **Path:** `events`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Create Event](https://developers.livestorm.co/reference/post_events)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.attributes.copy_from_event_id` | body | `string` | no |
| `data.attributes.owner_id` | body | `string` | no |
| `data.attributes.title` | body | `string` | no |
| `data.attributes.slug` | body | `string` | no |
| `data.attributes.status` | body | `string` | no |
| `data.attributes.everyone_can_speak` | body | `boolean` | no |
| `data.attributes.detailed_registration_page_enabled` | body | `boolean` | no |
| `data.attributes.light_registration_page_enabled` | body | `boolean` | no |
| `data.attributes.description` | body | `string` | no |
| `data.attributes.recording_enabled` | body | `boolean` | no |
| `data.attributes.recording_public` | body | `boolean` | no |
| `data.attributes.show_in_company_page` | body | `boolean` | no |
| `data.attributes.chat_enabled` | body | `boolean` | no |
| `data.attributes.questions_enabled` | body | `boolean` | no |
| `data.attributes.polls_enabled` | body | `boolean` | no |
| `data.relationships.sessions[]` | body | `array<object>` | no |
| `data.relationships.sessions[].type` | body | `string` | no |
| `data.relationships.sessions[].attributes.estimated_started_at` | body | `date` | no |
| `data.relationships.sessions[].attributes.timezone` | body | `string` | no |

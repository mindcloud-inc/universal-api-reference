# Update Event with Livestorm

Updates an existing event in Livestorm.

## Endpoint

- **Method:** `PATCH`
- **Path:** `events/:id`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Update Event](https://developers.livestorm.co/reference/patch_events-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Event ID |
| `data.attributes.owner_id` | body | `string` | no | — |
| `data.attributes.title` | body | `string` | no | — |
| `data.attributes.slug` | body | `string` | no | — |
| `data.attributes.status` | body | `string` | no | — |
| `data.attributes.everyone_can_speak` | body | `boolean` | no | — |
| `data.attributes.detailed_registration_page_enabled` | body | `boolean` | no | — |
| `data.attributes.light_registration_page_enabled` | body | `boolean` | no | — |
| `data.attributes.description` | body | `string` | no | — |
| `data.attributes.recording_enabled` | body | `boolean` | no | — |
| `data.attributes.recording_public` | body | `boolean` | no | — |
| `data.attributes.show_in_company_page` | body | `boolean` | no | — |
| `data.attributes.chat_enabled` | body | `boolean` | no | — |
| `data.attributes.questions_enabled` | body | `boolean` | no | — |
| `data.attributes.polls_enabled` | body | `boolean` | no | — |

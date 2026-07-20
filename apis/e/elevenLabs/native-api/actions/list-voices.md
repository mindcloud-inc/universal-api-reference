# List Voices with ElevenLabs

Retrieves a list of voices from ElevenLabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/voices`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [List Voices](https://elevenlabs.io/docs/api-reference/voices/search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `next_page_token` | query | `string` | no |
| `page_size` | query | `number` | no |
| `search` | query | `string` | no |
| `sort` | query | `string` | no |
| `sort_direction` | query | `string` | no |
| `voice_type` | query | `string` | no |
| `category` | query | `string` | no |
| `fine_tuning_state` | query | `string` | no |
| `collection_id` | query | `string` | no |
| `include_total_count` | query | `boolean` | no |
| `voice_ids` | query | `string` | no |

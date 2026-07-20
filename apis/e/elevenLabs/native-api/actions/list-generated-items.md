# List Generated Items with ElevenLabs

Retrieves previously generated audio from ElevenLabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/history`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [List Generated Items](https://elevenlabs.io/docs/api-reference/history/list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page_size` | query | `number` | no |
| `start_after_history_item_id` | query | `string` | no |
| `voice_id` | query | `string` | no |
| `model_id` | query | `string` | no |
| `date_before_unix` | query | `number` | no |
| `date_after_unix` | query | `number` | no |
| `sort_direction` | query | `string` | no |
| `search` | query | `string` | no |
| `source` | query | `string` | no |

# Send Call with Bland AI

Creates a new call in Bland AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/calls`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [Send Call](https://docs.bland.ai/api-v1/post/calls)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phone_number` | body | `string` | yes |
| `voice` | body | `string` | no |
| `pathway_id` | body | `string` | no |
| `pathway_version` | body | `number` | no |
| `task` | body | `string` | yes |
| `first_sentence` | body | `string` | no |
| `persona_id` | body | `string` | no |
| `model` | body | `string` | no |
| `language` | body | `string` | no |
| `wait_for_greeting` | body | `boolean` | no |
| `pronunciation_guide[]` | body | `array<string>` | no |
| `temperature` | body | `number` | no |
| `interruption_threshold` | body | `number` | no |
| `from` | body | `string` | no |
| `dialing_strategy` | body | `object` | no |
| `timezone` | body | `string` | no |
| `start_time` | body | `string` | no |
| `transfer_phone_number` | body | `string` | no |
| `transfer_list` | body | `object` | no |
| `max_duration` | body | `number` | no |
| `tools[]` | body | `array<string>` | no |
| `background_track` | body | `string` | no |
| `noise_cancellation` | body | `boolean` | no |
| `block_interruptions` | body | `boolean` | no |
| `record` | body | `boolean` | no |
| `voicemail` | body | `object` | no |
| `citation_schema_ids[]` | body | `array<string>` | no |
| `summary_prompt` | body | `string` | no |
| `retry` | body | `object` | no |
| `dispositions[]` | body | `array<string>` | no |
| `request_data` | body | `object` | no |
| `metadata` | body | `object` | no |
| `webhook` | body | `string` | no |
| `webhook_events[]` | body | `array<string>` | no |
| `dynamic_data[]` | body | `array<object>` | no |
| `keywords[]` | body | `array<string>` | no |
| `ignore_button_press` | body | `boolean` | no |
| `precall_dtmf_sequence` | body | `string` | no |
| `guard_rails[]` | body | `array<string>` | no |

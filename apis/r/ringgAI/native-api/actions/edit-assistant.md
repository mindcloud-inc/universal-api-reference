# Edit Assistant with Ringg AI

Updates an existing assistant in Ringg AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agent/v1`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Edit Assistant](https://docs.ringg.ai/api-reference/endpoint/assistant/edit-assistant)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `operation` | body | `string` | yes |
| `agent_id` | body | `string` | yes |
| `agent_display_name` | body | `string` | no |
| `language` | body | `string` | no |
| `voice_id` | body | `string` | no |
| `secondary_voice_id` | body | `string` | no |
| `secondary_language` | body | `string` | no |
| `agent_prompt` | body | `string` | no |
| `custom_variables[]` | body | `array<string>` | no |
| `number_id` | body | `string` | no |
| `kb_id` | body | `string` | no |
| `whitelisted_domains[]` | body | `array<string>` | no |
| `voice_speed` | body | `number` | no |

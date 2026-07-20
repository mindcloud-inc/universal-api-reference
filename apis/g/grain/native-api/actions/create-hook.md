# Create Hook with Grain

Creates a new hook in Grain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/hooks/create`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Create Hook](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hook_url` | body | `string` | yes | — |
| `include.ai_action_items` | body | `boolean` | no | Include AI action items in hook payloads. |
| `include.ai_summary` | body | `boolean` | no | Include AI summary in hook payloads. |
| `include.ai_template_sections` | body | `object` | no | Include AI template sections in hook payloads. |
| `include.ai_template_sections.allowed_sections[]` | body | `array<string>` | no | Only include AI template sections whose title matches one of these values. |
| `include.ai_template_sections.format` | body | `list` | no | Output format for AI template sections in hook payloads. Accepted values: `json`, `markdown`, `text`. |
| `include.calendar_event` | body | `boolean` | no | Include calendar event data in hook payloads. |
| `include.highlights` | body | `boolean` | no | Include clips/highlights in hook payloads. |
| `include.hubspot` | body | `boolean` | no | Include HubSpot related data in hook payloads. |
| `include.participants` | body | `boolean` | no | Include participants in hook payloads. |
| `include.private_notes` | body | `boolean` | no | Include private notes in hook payloads. |
| `include.speakers` | body | `boolean` | no | Include highlight speakers in hook payloads. |
| `include.transcript` | body | `boolean` | no | Include highlight transcript in hook payloads. |
| `hook_type` | body | `list` | yes | Accepted values: `highlight_added`, `highlight_deleted`, `highlight_updated`, `recording_added`, `recording_deleted`, `recording_updated`, `story_added`, `story_deleted`, `story_updated`, `upload_status`. |
| `include` | body | `object` | no | — |

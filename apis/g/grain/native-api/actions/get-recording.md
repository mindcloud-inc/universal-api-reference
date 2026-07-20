# Get Recording with Grain

Retrieves a recording from Grain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/recordings/:recording_id`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [Get Recording](https://developers.grain.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include.ai_action_items` | body | `boolean` | no | Include AI action items in the response. |
| `include.ai_summary` | body | `boolean` | no | Include AI summary in the response. |
| `include.ai_template_sections` | body | `object` | no | Include AI template sections in the response. |
| `include.ai_template_sections.allowed_sections[]` | body | `array<string>` | no | Only include AI template sections whose title matches one of these values. |
| `include.ai_template_sections.format` | body | `list` | no | Output format for AI template sections. Accepted values: `json`, `markdown`, `text`. |
| `include.calendar_event` | body | `boolean` | no | Include calendar event data in the response. |
| `include.highlights` | body | `boolean` | no | Include clips/highlights in the response. |
| `include.hubspot` | body | `boolean` | no | Include HubSpot related data in the response. |
| `include.participants` | body | `boolean` | no | Include participants in the response. |
| `include.private_notes` | body | `boolean` | no | Include private notes in the response. |
| `recording_id` | path | `list<string>` | yes | — |
| `include` | body | `object` | no | — |

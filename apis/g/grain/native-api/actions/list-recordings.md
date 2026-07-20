# List Recordings with Grain

Retrieves recordings from Grain.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/recordings`
- **Base URL:** `https://api.grain.com/_/public-api`
- **Official documentation:** [List Recordings](https://developers.grain.com/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.after_datetime` | body | `date` | no | Only return recordings whose start_datetime is before this timestamp, per Grain's Recording Filter docs. |
| `filter.before_datetime` | body | `date` | no | Only return recordings whose start_datetime is after this timestamp, per Grain's Recording Filter docs. |
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
| `include` | body | `object` | no | Optional related entities to include in response. |

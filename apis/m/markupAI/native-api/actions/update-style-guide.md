# Update Style Guide with Markup AI

Updates an existing style guide in Markup AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/style-guides/:style_guide_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Update Style Guide](https://docs.markup.ai/api-reference/style-guides/update-style-guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `style_guide_id` | path | `string` | yes | UUID of the style guide to update. |
| `name` | body | `string` | no | Updated style guide name. |
| `terminology_domain_ids[]` | body | `array<string>` | no | Updated terminology domain IDs for the style guide. |

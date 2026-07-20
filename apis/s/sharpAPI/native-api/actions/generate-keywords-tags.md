# Generate Keywords Tags with SharpAPI

Creates keywords and tags in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/keywords`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Keywords Tags](https://sharpapi.com/en/catalog/ai/content-marketing-automation/keywords-tags-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Content to analyze for keywords and tags. |
| `language` | body | `string` | no | Language for the generated keywords and tags. |
| `max_quantity` | body | `number` | no | Maximum number of keywords to generate. |
| `voice_tone` | body | `string` | no | Preferred tone for keyword generation. |
| `context` | body | `string` | no | Additional instructions for keyword generation. |

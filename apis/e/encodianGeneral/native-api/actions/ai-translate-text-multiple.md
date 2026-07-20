# AI Translate Text Multiple with Encodian - General

Translates multiple text strings with Encodian AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AITranslateTextMultiple`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Translate Text Multiple](https://support.encodian.com/hc/en-gb/articles/13670267593628)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to translate. |
| `targetLanguages[]` | body | `array<string>` | yes | Target languages to translate into. |

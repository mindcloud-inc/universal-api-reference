# Translate Text with SharpAPI

Creates a text translation job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/translate`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Translate Text](https://sharpapi.com/en/catalog/ai/content-marketing-automation/advanced-text-translator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Content to translate. |
| `language` | body | `string` | yes | Target language for the translated output. |
| `voice_tone` | body | `string` | no | Preferred tone of the translated output. |
| `context` | body | `string` | no | Additional processing instructions for the translation. |

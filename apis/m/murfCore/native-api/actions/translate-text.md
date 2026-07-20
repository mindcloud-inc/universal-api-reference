# Translate Text with Murf Core

Translates text into another language with Murf Core.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text/translate`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Translate Text](https://murf.ai/api/docs/api-reference/translation/translate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetLanguage` | body | `string` | yes | Language code for the translated output. |
| `texts[]` | body | `array<string>` | yes | List of source texts to translate. |

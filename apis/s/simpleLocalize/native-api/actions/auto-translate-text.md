# Auto-Translate Text with SimpleLocalize

Creates an auto-translation job for text in SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/auto-translate`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Auto-Translate Text](https://api.simplelocalize.io/openapi/ui#/Auto-translation/autoTranslateText)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetLanguage` | body | `string` | yes | Provider target language key |
| `targetProjectLanguage` | body | `string` | no | Project target language key (optional). It's required to load additional information about the target language (e.g. DeepL glossary). |
| `deeplFormality` | body | `list` | no | DeepL formality Accepted values: `default, more, less`. |
| `description` | body | `string` | no | Description that will be used as a context for translation. It's useful for better translation quality. |
| `translationProvider` | body | `list` | yes | Provider for auto-translation Accepted values: `DEEPL`, `GOOGLE_TRANSLATE`, `OPEN_AI`. |
| `sourceText` | body | `string` | yes | Source text to translate |
| `sourceProjectLanguage` | body | `string` | no | Project source language key (optional). It's required to load additional information about the source language (e.g. DeepL glossary). |
| `sourceLanguage` | body | `string` | no | Provider source language key (optional). If not provided, the source language will be detected automatically. |

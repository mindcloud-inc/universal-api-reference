# Translate content with 1minAI

Creates translated text content in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Translate content](https://docs.1min.ai/docs/api/ai-for-writing/content-translator/content-translator-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `originalLanguage` | body | `string` | no |
| `targetLanguage` | body | `string` | no |
| `tone` | body | `string` | no |
| `domain` | body | `string` | no |
| `writingStyle` | body | `string` | no |

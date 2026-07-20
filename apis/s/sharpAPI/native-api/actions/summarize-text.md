# Summarize Text with SharpAPI

Creates a text summary job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/summarize`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Summarize Text](https://sharpapi.com/en/catalog/ai/content-marketing-automation/summarize-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Content to summarize. |
| `voice_tone` | body | `string` | no | Preferred tone of the summary. |
| `max_length` | body | `number` | no | Suggested maximum summary length in words. |
| `language` | body | `string` | no | Language for the summarized output. |
| `context` | body | `string` | no | Additional processing instructions for the summary. |

# Detect AI Text with Winston AI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ai-content-detection`
- **Base URL:** `https://api.gowinston.ai`
- **Official documentation:** [Detect AI Text](https://docs.gowinston.ai/api-reference/v2/ai-content-detection/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text to scan for AI-generated content. |
| `file` | body | `string` | no | A public PDF, DOC, or DOCX URL to scan instead of raw text. |
| `website` | body | `string` | no | A public website URL to scan instead of raw text. |
| `version` | body | `string` | no | The Winston AI model version to use. |
| `sentences` | body | `boolean` | no | Include per-sentence scores in the response. |
| `language` | body | `string` | no | Two-letter language code, or auto for auto-detection. |

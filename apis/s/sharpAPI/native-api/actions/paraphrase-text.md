# Paraphrase Text with SharpAPI

Creates a text paraphrase job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/content/paraphrase`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Paraphrase Text](https://sharpapi.com/en/catalog/ai/content-marketing-automation/paraphrase-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Content to paraphrase. |
| `language` | body | `string` | no | Language for the paraphrased output. |
| `voice_tone` | body | `string` | no | Preferred tone of the paraphrased output. |
| `max_length` | body | `number` | no | Suggested maximum length of the paraphrased text. |
| `context` | body | `string` | no | Additional instructions for the paraphrase. |

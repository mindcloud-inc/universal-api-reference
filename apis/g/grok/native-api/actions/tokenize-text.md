# Tokenize Text with Grok

Creates a tokenized representation of text in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tokenize-text`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Tokenize Text](https://docs.x.ai/developers/rest-api-reference/inference/other#tokenize-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model ID to tokenize with. |
| `text` | body | `string` | yes | Text content to tokenize. |
| `user` | body | `string` | no | Optional user identifier. |

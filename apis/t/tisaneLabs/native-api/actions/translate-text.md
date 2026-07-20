# Translate Text with Tisane Labs

Translates input text in Tisane Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/transform`
- **Base URL:** `https://api.tisane.ai`
- **Official documentation:** [Translate Text](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/transform)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | IETF tag for the source language, or * / a vertical-bar-delimited set for autodetect. |
| `to` | body | `string` | yes | IETF tag for the target language. |
| `content` | body | `string` | yes | Text content to translate or paraphrase. |
| `settings` | body | `object` | no | Optional translation settings object. |

# Analyze Text with Tisane Labs

Analyzes input text in Tisane Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/parse`
- **Base URL:** `https://api.tisane.ai`
- **Official documentation:** [Analyze Text](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/parse)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | yes | Language code for the text to analyze. |
| `content` | body | `string` | yes | Text content to analyze. |
| `settings` | body | `object` | no | Optional Tisane analysis settings object. |

# Detect Language with Tisane Labs

Detects input language in Tisane Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/detectLanguage`
- **Base URL:** `https://api.tisane.ai`
- **Official documentation:** [Detect Language](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/detectLanguage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Text fragment to analyze for language detection. |
| `languages` | body | `string` | no | Optional vertical-bar-delimited language codes to use as cues. |
| `delimiter` | body | `string` | no | Optional regular expression for segmenting the fragment. |

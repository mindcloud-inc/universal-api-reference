# Extract Text with Tisane Labs

Extracts plain text from HTML in Tisane Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/helper/extract_text`
- **Base URL:** `https://api.tisane.ai`
- **Official documentation:** [Extract Text](https://docs.tisane.ai/apis/tisane-api-short#tag/NLU-/-NLP-Methods/operation/extract_text)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Markup or text content from which readable text will be extracted. |

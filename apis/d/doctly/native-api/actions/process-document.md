# Process Document with Doctly

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.doctly.ai/api/v1`
- **Official documentation:** [Process Document](https://docs.doctly.ai/api-reference/documents/process)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | Document file to process. Provide either file or URL. |
| `url` | body | `string` | no | Public document URL to fetch and process. Provide either URL or file. |
| `accuracy` | body | `string` | no | Processing accuracy level: lite or ultra. |
| `extractor_id` | body | `string` | no | Optional extractor UUID to use instead of standard Markdown conversion. |
| `page_separator` | body | `boolean` | no | Include page break markers in Markdown output. |
| `skip_images` | body | `boolean` | no | Skip image extraction and transcription. |
| `callback_url` | body | `string` | no | HTTPS webhook URL to notify when processing completes. |

# Upload File to ConvertAPI with Text to pdf

Uploads a file to Text to PDF for later conversion.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/execute/TEXT_TO_PDF_UPLOAD_FILE`
- **Base URL:** `https://backend.composio.dev/api/v3`
- **Official documentation:** [Upload File to ConvertAPI](https://docs.composio.dev/toolkits/text_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments` | body | `object` | no | Tool input arguments object. |
| `arguments.url` | body | `string` | no | Remote file URL to upload to ConvertAPI server. |
| `arguments.file` | body | `file` | no | MindCloud file object to upload to ConvertAPI server. |
| `arguments.file_id` | body | `string` | no | Optional custom lowercase alphanumeric id for the uploaded file. |
| `arguments.filename` | body | `string` | no | Optional filename override for the uploaded file. |
| `arguments.header_name` | body | `string` | no | Optional header name for fetching a protected remote URL. |
| `arguments.header_value` | body | `string` | no | Optional header value for fetching a protected remote URL. |

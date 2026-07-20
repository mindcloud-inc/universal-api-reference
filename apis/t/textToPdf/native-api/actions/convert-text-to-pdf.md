# Convert Text to PDF with Text to pdf

Creates a PDF document from text in Text to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/execute/TEXT_TO_PDF_CONVERT_TEXT_TO_PDF`
- **Base URL:** `https://backend.composio.dev/api/v3`
- **Official documentation:** [Convert Text to PDF](https://docs.composio.dev/toolkits/text_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments` | body | `object` | yes | Tool input arguments object. |
| `arguments.text` | body | `string` | yes | The complete plain text or Markdown content to convert to PDF. |
| `arguments.file_type` | body | `list` | yes | Input text format. Accepted values are txt and markdown. Accepted values: `Markdown`, `Plain text`. |

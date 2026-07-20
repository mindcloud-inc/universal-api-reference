# Download File with Text to pdf

Retrieves a file from Text to PDF by file ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/execute/TEXT_TO_PDF_DOWNLOAD_FILE`
- **Base URL:** `https://backend.composio.dev/api/v3`
- **Official documentation:** [Download File](https://docs.composio.dev/toolkits/text_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments` | body | `object` | yes | Tool input arguments object. |
| `arguments.file_id` | body | `string` | yes | Unique file id returned from upload or conversion. |
| `arguments.download` | body | `list` | no | Download behavior: attachment or inline. Accepted values: `Attachment`, `Inline`. |

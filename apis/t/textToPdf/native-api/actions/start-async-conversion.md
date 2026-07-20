# Start Async Conversion with Text to pdf

Starts an asynchronous file conversion job in Text to PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/execute/TEXT_TO_PDF_START_ASYNC_CONVERSION`
- **Base URL:** `https://backend.composio.dev/api/v3`
- **Official documentation:** [Start Async Conversion](https://docs.composio.dev/toolkits/text_to_pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments` | body | `object` | yes | Tool input arguments object. |
| `arguments.from_format` | body | `string` | yes | Source file format, such as txt, docx, or html. |
| `arguments.to_format` | body | `string` | yes | Target output format, such as pdf. |
| `arguments.file` | body | `string` | yes | Public file URL or file content to convert. |
| `arguments.job_id` | body | `string` | no | Optional custom 32-character lowercase alphanumeric job id. |
| `arguments.webhook` | body | `string` | no | Optional callback URL for conversion completion notification. |

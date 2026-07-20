# Text to pdf: Native API Reference

A consolidated summary of Text to pdf's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.composio.dev/toolkits/text_to_pdf
- **API base URL:** `https://backend.composio.dev/api/v3`

## Authentication

### Composio API key

Composio project API key sent in the x-api-key request header.

### Credentials

- **API Key:** `apiKey` · required · Composio project API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.composio.dev/reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `408,429,500,502,503`. Wait 1000 ms before the first retry. Stop after 2 attempts.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Text to PDF](actions/convert-text-to-pdf.md) | `POST /tools/execute/TEXT_TO_PDF_CONVERT_TEXT_TO_PDF` | [docs](https://docs.composio.dev/toolkits/text_to_pdf) |
| [Delete Async Job](actions/delete-async-job.md) | `POST /tools/execute/TEXT_TO_PDF_DELETE_ASYNC_JOB` | [docs](https://docs.composio.dev/toolkits/text_to_pdf) |
| [Delete File](actions/delete-file.md) | `POST /tools/execute/TEXT_TO_PDF_DELETE_FILE` | [docs](https://docs.composio.dev/toolkits/text_to_pdf) |
| [Download File](actions/download-file.md) | `POST /tools/execute/TEXT_TO_PDF_DOWNLOAD_FILE` | [docs](https://docs.composio.dev/toolkits/text_to_pdf) |
| [Start Async Conversion](actions/start-async-conversion.md) | `POST /tools/execute/TEXT_TO_PDF_START_ASYNC_CONVERSION` | [docs](https://docs.composio.dev/toolkits/text_to_pdf) |
| [Upload File to ConvertAPI](actions/upload-file-to-convert-api.md) | `POST /tools/execute/TEXT_TO_PDF_UPLOAD_FILE` | [docs](https://docs.composio.dev/toolkits/text_to_pdf) |

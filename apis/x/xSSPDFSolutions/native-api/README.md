# XSS PDF Solutions: Native API Reference

A consolidated summary of XSS PDF Solutions's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/
- **API base URL:** `https://api.xss-cross-service-solutions.com/solutions/solutions`

## Authentication

### API Key

Authenticate with a Cross Service Solutions API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask PDF With AI](actions/ask-pdf-with-ai.md) | `POST /api/27` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#ask-pdf-with-ai) |
| [Compress PDF](actions/compress-pdf.md) | `POST /api/29` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#compress-pdf) |
| [Convert to PDF](actions/convert-to-pdf.md) | `POST /api/31` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#convert-to-pdf) |
| [Flatten PDF](actions/flatten-pdf.md) | `POST /api/41` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#flatten-pdf) |
| [Merge Multiple PDFs](actions/merge-multiple-pd-fs.md) | `POST /api/30` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#merge-multiple-pdfs) |
| [Protect PDF](actions/protect-pdf.md) | `POST /api/32` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#protect-pdf) |
| [Remove Metadata from PDF](actions/remove-metadata-from-pdf.md) | `POST /api/40` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#remove-metadata-from-pdf) |
| [Unlock PDF](actions/unlock-pdf.md) | `POST /api/33` | [docs](https://learn.microsoft.com/en-us/connectors/xsspdfsolutionsinteg/#unlock-pdf) |

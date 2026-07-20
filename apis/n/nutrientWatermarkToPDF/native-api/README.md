# Nutrient - Watermark to PDF: Native API Reference

A consolidated summary of Nutrient - Watermark to PDF's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/
- **OpenAPI specification:** https://www.nutrient.io/api/documentation/developer-guides/api-reference/
- **API base URL:** `https://api.nutrient.io`

## Authentication

### API Key

Authenticate requests with a Nutrient DWS Processor API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nutrient.io/guides/dws-processor/developer-guides/authentication/)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Image Watermark to PDF](actions/add-image-watermark-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/) |
| [Add Last Page Watermark to PDF](actions/add-last-page-watermark-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/) |
| [Add Multiple Watermarks to PDF](actions/add-multiple-watermarks-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/) |
| [Add Page Range Watermark to PDF](actions/add-page-range-watermark-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/) |
| [Add Text Watermark to PDF](actions/add-text-watermark-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/) |

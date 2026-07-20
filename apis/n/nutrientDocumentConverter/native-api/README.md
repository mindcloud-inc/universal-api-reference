# Nutrient Document Converter: Native API Reference

A consolidated summary of Nutrient Document Converter's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://www.nutrient.io/guides/dws-processor/
- **OpenAPI specification:** https://www.nutrient.io/api/documentation/developer-guides/api-reference/
- **API base URL:** `https://api.nutrient.io`

## Authentication

### API key

Authenticate to Nutrient DWS Processor with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nutrient.io/guides/dws-processor/developer-guides/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md) | `POST /processor/md_to_pdf` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/markdown-to-pdf-api/) |
| [Convert Remote Document to Image](actions/convert-remote-document-to-image.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/document-to-image-api/) |
| [Convert Remote Document to PDF](actions/convert-remote-document-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/developer-guides/) |
| [Convert Remote Image to PDF](actions/convert-remote-image-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/image-to-pdf-api/) |
| [Convert Remote PDF to Image](actions/convert-remote-pdf-to-image.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-to-image-api/) |
| [Convert Remote PDF to PDF/A](actions/convert-remote-pdf-to-pdfa.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-to-pdfa-api/) |
| [Flatten Remote PDF](actions/flatten-remote-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/developer-guides/) |
| [Generate PDF from Remote HTML](actions/generate-pdf-from-remote-html.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-generator-api/) |
| [OCR Remote Document](actions/ocr-remote-document.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-ocr-api/) |
| [Protect Remote PDF](actions/protect-remote-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-security-api/) |
| [Run Build Instructions](actions/run-build-instructions.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/developer-guides/) |
| [Watermark Remote PDF](actions/watermark-remote-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-watermark-api/) |

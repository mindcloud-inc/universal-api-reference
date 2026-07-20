# Nutrient - Convert to PDF: Native API Reference

A consolidated summary of Nutrient - Convert to PDF's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.nutrient.io/api/pdf-converter-api/
- **OpenAPI specification:** https://www.nutrient.io/api/documentation/developer-guides/api-reference/
- **API base URL:** `https://api.nutrient.io`

## Authentication

### API Key

Authenticate requests with a Nutrient DWS Processor API key using bearer token authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nutrient.io/api/documentation/developer-guides/authentication/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert HTML File to PDF](actions/convert-html-file-to-pdf.md) | `POST /processor/generate_pdf` | [docs](https://www.nutrient.io/api/html-to-pdf-api/) |
| [Convert Image to PDF](actions/convert-image-to-pdf.md) | `POST /processor/convert_to_pdf` | [docs](https://www.nutrient.io/api/image-to-pdf-api/) |
| [Convert Markdown to PDF](actions/convert-markdown-to-pdf.md) | `POST /processor/md_to_pdf` | [docs](https://www.nutrient.io/api/md-to-pdf-api/) |
| [Convert Office Document to PDF](actions/convert-office-document-to-pdf.md) | `POST /processor/convert_to_pdf` | [docs](https://www.nutrient.io/api/office-to-pdf-api/) |
| [Convert URL File to PDF](actions/convert-url-file-to-pdf.md) | `POST /build` | [docs](https://www.nutrient.io/api/url-to-pdf-api/) |
| [Convert URL File to PDF/A](actions/convert-url-file-to-pdfa.md) | `POST /build` | [docs](https://www.nutrient.io/api/pdf-to-pdfa-api/) |

# Nutrient - Extract from PDF: Native API Reference

A consolidated summary of Nutrient - Extract from PDF's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.nutrient.io/api/extract-text-from-pdf-api/
- **API base URL:** `https://api.nutrient.io`

## Authentication

### API Key

Authenticate Nutrient DWS Processor API requests with a bearer API key.

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
| [Convert PDF to Markdown](actions/convert-pdf-to-markdown.md) | `POST /build` | [docs](https://www.nutrient.io/api/pdf-to-md-api/) |
| [Extract PDF Plain Text](actions/extract-pdf-plain-text.md) | `POST /build` | [docs](https://www.nutrient.io/api/extract-text-from-pdf-api/) |
| [Extract PDF Structured Text](actions/extract-pdf-structured-text.md) | `POST /build` | [docs](https://www.nutrient.io/api/extract-text-from-pdf-api/) |
| [Extract PDF Tables as JSON](actions/extract-pdf-tables-as-json.md) | `POST /build` | [docs](https://www.nutrient.io/api/pdf-to-json-api/) |
| [Extract PDF Text](actions/extract-pdf-text.md) | `POST /build` | [docs](https://www.nutrient.io/api/extract-text-from-pdf-api/) |

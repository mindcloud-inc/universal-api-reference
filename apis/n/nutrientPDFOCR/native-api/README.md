# Nutrient - PDF OCR: Native API Reference

A consolidated summary of Nutrient - PDF OCR's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-ocr-api/
- **API base URL:** `https://api.nutrient.io`

## Authentication

### API Key

Authenticate requests with a Nutrient DWS Processor API key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.nutrient.io/guides/dws-processor/getting-started/)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/pdf` |
| `Content-Type` | `multipart/form-data` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [OCR Document](actions/ocr-document.md) | `POST /processor/ocr` | [docs](https://www.nutrient.io/guides/dws-processor/tools-and-api/pdf-ocr-api/) |

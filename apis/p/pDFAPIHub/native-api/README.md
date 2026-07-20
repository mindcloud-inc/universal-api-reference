# PDF API Hub: Native API Reference

A consolidated summary of PDF API Hub's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api.prefillpdf.com/docs
- **OpenAPI specification:** https://api.prefillpdf.com/openapi.json
- **API base URL:** `https://api.prefillpdf.com`

## Authentication

### API Key

Connect with your PDF API Hub API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.prefillpdf.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract CSV From File](actions/extract-csv-from-file.md) | `POST /extract-csv` | [docs](https://api.prefillpdf.com/docs#/PDF%20Tools/extract_csv_endpoint_extract_csv_post) |
| [Extract Text From File](actions/extract-text-from-file.md) | `POST /extract-text` | [docs](https://api.prefillpdf.com/docs#/PDF%20Tools/extract_text_endpoint_extract_text_post) |
| [Extract Text From URL](actions/extract-text-from-url.md) | `POST /extract-text-from-url` | [docs](https://api.prefillpdf.com/docs#/PDF%20Tools/extract_text_from_url_endpoint_extract_text_from_url_post) |
| [Fill PDF](actions/fill-pdf.md) | `POST /fill-pdf` | [docs](https://api.prefillpdf.com/docs#/PDF%20Tools/fill_pdf_endpoint_fill_pdf_post) |
| [Watermark PDF](actions/watermark-pdf.md) | `POST /watermark` | [docs](https://api.prefillpdf.com/docs#/PDF%20Tools/watermark_endpoint_watermark_post) |

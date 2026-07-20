# Pdfless: Native API Reference

A consolidated summary of Pdfless's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.pdfless.com/
- **API base URL:** `https://api.pdfless.com`

## Authentication

### API Key

Authenticate with a Pdfless API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pdfless.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | `POST /v1/pdfs` | [docs](https://docs.pdfless.com/pdfs) |

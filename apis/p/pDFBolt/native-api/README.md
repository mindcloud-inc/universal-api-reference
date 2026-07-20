# PDFBolt: Native API Reference

A consolidated summary of PDFBolt's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://pdfbolt.com/docs
- **API base URL:** `https://api.pdfbolt.com/v1`

## Authentication

### API Key

Authenticate with your PDFBolt API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
API-KEY: <apiKey>
```

[Official authentication documentation](https://pdfbolt.com/docs/admin-dashboard/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create PDF from HTML](actions/create-pdf-from-html.md) | `POST /direct` | [docs](https://pdfbolt.com/docs/api-endpoints/direct) |
| [Create PDF from Template](actions/create-pdf-from-template.md) | `POST /direct` | [docs](https://pdfbolt.com/docs/api-endpoints/direct) |
| [Create PDF from URL](actions/create-pdf-from-url.md) | `POST /direct` | [docs](https://pdfbolt.com/docs/api-endpoints/direct) |
| [Create PDF Link from HTML](actions/create-pdf-link-from-html.md) | `POST /sync` | [docs](https://pdfbolt.com/docs/api-endpoints/sync) |
| [Create PDF Link from Template](actions/create-pdf-link-from-template.md) | `POST /sync` | [docs](https://pdfbolt.com/docs/api-endpoints/sync) |
| [Create PDF Link from URL](actions/create-pdf-link-from-url.md) | `POST /sync` | [docs](https://pdfbolt.com/docs/api-endpoints/sync) |
| [Get Usage](actions/get-usage.md) | `GET /usage` | [docs](https://pdfbolt.com/docs/api-endpoints/usage-monitoring) |

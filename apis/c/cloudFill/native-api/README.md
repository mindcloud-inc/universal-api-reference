# CloudFill: Native API Reference

A consolidated summary of CloudFill's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.cloudfill.io/help/
- **OpenAPI specification:** https://api.swaggerhub.com/apis/hpoul/CloudFill/1.3
- **API base URL:** `https://api.cloudfill.io`

## Authentication

### API Key

Use a CloudFill API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://www.cloudfill.io/help/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate PDF](actions/generate-pdf.md) | `POST /api/pdf/{pdfKey}/generate` | [docs](https://api.swaggerhub.com/apis/hpoul/CloudFill/1.3) |
| [Get PDF Details](actions/get-pdf-details.md) | `GET /api/meta/pdf/{pdfKey}` | [docs](https://api.swaggerhub.com/apis/hpoul/CloudFill/1.3) |
| [List PDFs](actions/list-pdfs.md) | `GET /api/meta/pdf/` | [docs](https://api.swaggerhub.com/apis/hpoul/CloudFill/1.3) |

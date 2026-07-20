# HTML to PDF: Native API Reference

A consolidated summary of HTML to PDF's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://platform.htmltopdfapi.co/docs/api
- **API base URL:** `https://platform.htmltopdfapi.co/api/v1`

## Authentication

### API Key

Use your HTML to PDF API key. MindCloud sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.htmltopdfapi.co/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate PDF from HTML](actions/generate-pdf-from-html.md) | `POST /pdf/generate` | [docs](https://platform.htmltopdfapi.co/docs/api#/GeneratePdf/post_pdf_generate) |
| [Generate PDF from URL](actions/generate-pdf-from-url.md) | `POST /pdf/generate` | [docs](https://platform.htmltopdfapi.co/docs/api#/GeneratePdf/post_pdf_generate) |
| [Validate API Key](actions/validate-api-key.md) | `GET /check` | [docs](https://platform.htmltopdfapi.co/docs/api#/CheckApiKey/get_check) |

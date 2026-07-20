# PDF-API.io: Native API Reference

A consolidated summary of PDF-API.io's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://pdf-api.io/en/docs
- **API base URL:** `https://pdf-api.io/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pdf-api.io/en/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | `GET /templates/:template` | [docs](https://pdf-api.io/en/docs/api/get-template) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://pdf-api.io/en/docs/api/templates) |
| [Merge Templates](actions/merge-templates.md) | `POST /templates/merge` | [docs](https://pdf-api.io/en/docs/api/merge-templates) |
| [Render PDF from Template](actions/render-pdf-from-template.md) | `POST /templates/:templateId/pdf` | [docs](https://pdf-api.io/en/docs/api/render-pdf) |

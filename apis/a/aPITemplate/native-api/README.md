# API Template: Native API Reference

A consolidated summary of API Template's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://apitemplate.io/apiv2/
- **API base URL:** `https://rest.apitemplate.io`

## Authentication

### API Key

Authenticate with your APITemplate.io API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://apitemplate.io/apiv2/#section/Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 300). Use `offset` in the query string as the record offset.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | `POST /v2/create-image` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-image) |
| [Create PDF](actions/create-pdf.md) | `POST /v2/create-pdf` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-pdf) |
| [Create PDF From HTML](actions/create-pdf-from-html.md) | `POST /v2/create-pdf-from-html` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-pdf-from-html) |
| [Create PDF From URL](actions/create-pdf-from-url.md) | `POST /v2/create-pdf-from-url` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/create-pdf-from-url) |
| [Delete Object](actions/delete-object.md) | `GET /v2/delete-object` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/delete-object) |
| [Get Template](actions/get-template.md) | `GET /v2/get-template` | [docs](https://apitemplate.io/apiv2/#tag/Template-Management/operation/get-template) |
| [List Generated Objects](actions/list-generated-objects.md) | `GET /v2/list-objects` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/list-objects) |
| [List Templates](actions/list-templates.md) | `GET /v2/list-templates` | [docs](https://apitemplate.io/apiv2/#tag/Template-Management/operation/list-templates) |
| [Merge PDFs](actions/merge-pdfs.md) | `POST /v2/merge-pdfs` | [docs](https://apitemplate.io/apiv2/#tag/PDF-Manipulation-API/operation/merge-pdfs) |
| [Query Account Information](actions/query-account-information.md) | `GET /v2/account-information` | [docs](https://apitemplate.io/apiv2/#tag/API-Integration/operation/account-information) |
| [Update PDF Template](actions/update-pdf-template.md) | `POST /v2/update-template` | [docs](https://apitemplate.io/apiv2/#tag/Template-Management/operation/update-template) |

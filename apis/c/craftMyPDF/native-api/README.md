# CraftMyPDF: Native API Reference

A consolidated summary of CraftMyPDF's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://craftmypdf.com/docs/index.html
- **OpenAPI specification:** https://craftmypdf.s3.ap-southeast-1.amazonaws.com/craftmypdf_api/craftmypdf_api.yaml
- **API base URL:** `https://api.craftmypdf.com/v1`

## Authentication

### API Key

Connect with your CraftMyPDF API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://craftmypdf.com/docs/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add text to a PDF](actions/add-text-to-apdf.md) | `POST /add-text-to-pdf` | [docs](https://craftmypdf.com/docs/index.html) |
| [Add watermark to a PDF](actions/add-watermark-to-apdf.md) | `POST /add-watermark` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create a new template](actions/create-a-new-template.md) | `POST /new-template-from` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create an image](actions/create-an-image.md) | `POST /create-image` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create a PDF](actions/create-apdf.md) | `POST /create` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create a PDF asynchronously](actions/create-apdf-asynchronously.md) | `POST /create-async` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create editor session](actions/create-editor-session.md) | `POST /create-editor-session` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create PDFs parallelly](actions/create-pd-fs-parallelly.md) | `POST /create-parallel` | [docs](https://craftmypdf.com/docs/index.html) |
| [Create PDF from templates](actions/create-pdf-from-templates.md) | `POST /create-merge` | [docs](https://craftmypdf.com/docs/index.html) |
| [Deactivate editor session](actions/deactivate-editor-session.md) | `POST /deactivate-editor-session` | [docs](https://craftmypdf.com/docs/index.html) |
| [Delete template](actions/delete-template.md) | `GET /delete-template` | [docs](https://craftmypdf.com/docs/index.html) |
| [Get account information](actions/get-account-information.md) | `GET /get-account-info` | [docs](https://craftmypdf.com/docs/index.html) |
| [Get PDF Information](actions/get-pdf-information.md) | `GET /get-pdf-info` | [docs](https://craftmypdf.com/docs/index.html) |
| [Get template](actions/get-template.md) | `GET /get-template` | [docs](https://craftmypdf.com/docs/index.html) |
| [List template versions](actions/list-template-versions.md) | `GET /list-template-versions` | [docs](https://craftmypdf.com/docs/index.html) |
| [List templates](actions/list-templates.md) | `GET /list-templates` | [docs](https://craftmypdf.com/docs/index.html) |
| [List transactions](actions/list-transactions.md) | `GET /list-transactions` | [docs](https://craftmypdf.com/docs/index.html) |
| [Merge PDF URLs](actions/merge-pdfur-ls.md) | `POST /merge-pdfs` | [docs](https://craftmypdf.com/docs/index.html) |
| [Query template usage](actions/query-template-usage.md) | `GET /query-template-usage` | [docs](https://craftmypdf.com/docs/index.html) |
| [Retain template versions](actions/retain-template-versions.md) | `POST /retain-template-versions` | [docs](https://craftmypdf.com/docs/index.html) |
| [Transfer a template](actions/transfer-a-template.md) | `POST /transfer-template-to` | [docs](https://craftmypdf.com/docs/index.html) |
| [Update fillable fields](actions/update-fillable-fields.md) | `POST /update-pdf-fields` | [docs](https://craftmypdf.com/docs/index.html) |
| [Update template](actions/update-template.md) | `POST /update-template` | [docs](https://craftmypdf.com/docs/index.html) |

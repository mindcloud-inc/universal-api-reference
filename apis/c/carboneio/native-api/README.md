# Carbone.io: Native API Reference

A consolidated summary of Carbone.io's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://carbone.io/documentation/developer/http-api/introduction.html
- **OpenAPI specification:** https://carbone.io/file/carbone.OpenAPI.yml
- **API base URL:** `https://api.carbone.io`

## Authentication

### API Key

Use a Carbone Cloud API key from your account home page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://carbone.io/documentation/developer/http-api/introduction.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `nextCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Document](actions/convert-document.md) | `POST /render/template` | [docs](https://carbone.io/documentation/developer/http-api/generate-reports.html#generate-a-report) |
| [Delete Template](actions/delete-template.md) | `DELETE /template/[:templateId-or-versionId]` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#delete-a-template) |
| [Download Template](actions/download-template.md) | `GET /template/[:templateId-or-versionId]` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#download-a-template) |
| [Generate Document](actions/generate-document.md) | `POST /render/[:templateId-or-versionId]` | [docs](https://carbone.io/documentation/developer/http-api/generate-reports.html#generate-a-report) |
| [Get Status](actions/get-status.md) | `GET /status` | [docs](https://carbone.io/documentation/developer/http-api/introduction.html) |
| [List Template Categories](actions/list-template-categories.md) | `GET /templates/categories` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#list-categories) |
| [List Template Tags](actions/list-template-tags.md) | `GET /templates/tags` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#list-tags) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#list-templates) |
| [Retrieve Generated Document](actions/retrieve-generated-document.md) | `GET /render/:renderId` | [docs](https://carbone.io/documentation/developer/http-api/download-reports.html) |
| [Update Template](actions/update-template.md) | `PATCH /template/[:templateId-or-versionId]` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#patch-a-template) |
| [Upload Template](actions/upload-template.md) | `POST /template` | [docs](https://carbone.io/documentation/developer/http-api/manage-templates.html#upload-a-template) |

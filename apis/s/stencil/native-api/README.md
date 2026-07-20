# Stencil: Native API Reference

A consolidated summary of Stencil's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.usestencil.com/api/authentication
- **API base URL:** `https://api.usestencil.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.usestencil.com/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `after` in the query string as the pagination cursor.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection Images](actions/create-collection-images.md) | `POST /v1/collections` | [docs](https://docs.usestencil.com/api/endpoints/collections#create-images-from-a-template-collection) |
| [Create Editor Session](actions/create-editor-session.md) | `POST /v1/editor/sessions` | [docs](https://docs.usestencil.com/api/endpoints/editor-session#create-a-new-session) |
| [Create Image](actions/create-image.md) | `POST /v1/images` | [docs](https://docs.usestencil.com/api/endpoints/image#create-image-asynchronously) |
| [Create Image Synchronously](actions/create-image-synchronously.md) | `POST /v1/images/sync` | [docs](https://docs.usestencil.com/api/endpoints/image#create-image-synchronously) |
| [Create PDF](actions/create-pdf.md) | `POST /v1/pdfs` | [docs](https://docs.usestencil.com/api/endpoints/pdfs#create-a-pdf-asynchronously) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://docs.usestencil.com/api/endpoints/account#account-information) |
| [Get Airtable Image Generation Status](actions/get-airtable-image-generation-status.md) | `GET /v1/airtables/:id` | [docs](https://docs.usestencil.com/api/endpoints/airtable#get-airtable-image-generation-status) |
| [Get Editor Session](actions/get-editor-session.md) | `GET /v1/editor/sessions/:session_id` | [docs](https://docs.usestencil.com/api/endpoints/editor-session#get-a-session) |
| [Get PDF](actions/get-pdf.md) | `GET /v1/pdfs/:pdf_id` | [docs](https://docs.usestencil.com/api/endpoints/pdfs#get-the-pdf) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:id` | [docs](https://docs.usestencil.com/api/endpoints/projects#get-specific-project) |
| [Get Template](actions/get-template.md) | `GET /v1/templates/:id` | [docs](https://docs.usestencil.com/api/endpoints/templates#get-specific-template) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects` | [docs](https://docs.usestencil.com/api/endpoints/projects#list-available-projects) |
| [List Templates](actions/list-templates.md) | `GET /v1/projects/:project_id/templates` | [docs](https://docs.usestencil.com/api/endpoints/templates#list-templates) |
| [Retrieve Collection Images](actions/retrieve-collection-images.md) | `GET /v1/collections/:id` | [docs](https://docs.usestencil.com/api/endpoints/collections#retrieve-images-from-template-collection) |
| [Search Images](actions/search-images.md) | `POST /v1/images/search` | [docs](https://docs.usestencil.com/api/endpoints/image#search-generated-images) |
| [Search PDFs](actions/search-pdfs.md) | `POST /v1/pdfs/search` | [docs](https://docs.usestencil.com/api/endpoints/pdfs#search-generated-pdfs) |
| [Trigger Airtable Image Generation](actions/trigger-airtable-image-generation.md) | `POST /v1/airtables/:id` | [docs](https://docs.usestencil.com/api/endpoints/airtable#trigger-airtable-image-generation-from-the-api) |

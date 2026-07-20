# Docutray: Native API Reference

A consolidated summary of Docutray's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.docutray.com/docs/api
- **OpenAPI specification:** https://docs.docutray.com/swagger.json
- **API base URL:** `https://app.docutray.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.docutray.com/docs/getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `pagination.total`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Upload Knowledge Base Documents](actions/bulk-upload-knowledge-base-documents.md) | `POST api/knowledge-bases/:id/documents/bulk-upload` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Convert Document](actions/convert-document.md) | `POST api/convert` | [docs](https://docs.docutray.com/docs/operations/convert) |
| [Start Document Conversion](actions/convert-document-async.md) | `POST api/convert-async` | [docs](https://docs.docutray.com/docs/operations/convert) |
| [Create Document Type](actions/create-document-type.md) | `POST api/document-types` | [docs](https://docs.docutray.com/docs/operations/document-types) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST api/knowledge-bases` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | `DELETE api/knowledge-bases/:id` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Delete Knowledge Base Document](actions/delete-knowledge-base-document.md) | `DELETE api/knowledge-bases/:id/documents/:documentId` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Start Step Execution](actions/execute-step-async.md) | `POST api/steps-async/:stepId` | [docs](https://docs.docutray.com/docs/operations/steps) |
| [Get Conversion Status](actions/get-conversion-status.md) | `GET api/convert-async/status/:id` | [docs](https://docs.docutray.com/docs/operations/convert) |
| [Get Document Type](actions/get-document-type.md) | `GET api/document-types/:id` | [docs](https://docs.docutray.com/docs/operations/document-types) |
| [Get Identification Status](actions/get-identification-status.md) | `GET api/identify-async/status/:id` | [docs](https://docs.docutray.com/docs/operations/identify) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET api/knowledge-bases/:id` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Get Knowledge Base Document](actions/get-knowledge-base-document.md) | `GET api/knowledge-bases/:id/documents/:documentId` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Get Step Execution Status](actions/get-step-execution-status.md) | `GET api/steps-async/status/:executionId` | [docs](https://docs.docutray.com/docs/operations/steps) |
| [Identify Document](actions/identify-document.md) | `POST api/identify` | [docs](https://docs.docutray.com/docs/operations/identify) |
| [Start Document Identification](actions/identify-document-async.md) | `POST api/identify-async` | [docs](https://docs.docutray.com/docs/operations/identify) |
| [List Document Types](actions/list-document-types.md) | `GET api/document-types` | [docs](https://docs.docutray.com/docs/api/document-types/listDocumentTypes) |
| [List Knowledge Base Documents](actions/list-knowledge-base-documents.md) | `GET api/knowledge-bases/:id/documents` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET api/knowledge-bases` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Advanced Search Knowledge Base](actions/search-knowledge-base.md) | `POST api/knowledge-bases/:id/search` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Search Knowledge Base](actions/search-knowledge-base-get.md) | `GET api/knowledge-bases/:id/search` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Sync Knowledge Base](actions/sync-knowledge-base.md) | `POST api/knowledge-bases/:id/sync` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Update Document Type](actions/update-document-type.md) | `PUT api/document-types/:id` | [docs](https://docs.docutray.com/docs/operations/document-types) |
| [Update Knowledge Base](actions/update-knowledge-base.md) | `PUT api/knowledge-bases/:id` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Update Knowledge Base Document](actions/update-knowledge-base-document.md) | `PUT api/knowledge-bases/:id/documents/:documentId` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Upload Knowledge Base Document](actions/upload-knowledge-base-document.md) | `POST api/knowledge-bases/:id/documents` | [docs](https://docs.docutray.com/docs/operations/knowledge-bases) |
| [Validate Document Type](actions/validate-document.md) | `POST api/document-types/:id/validate` | [docs](https://docs.docutray.com/docs/operations/document-types) |

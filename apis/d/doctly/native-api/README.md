# Doctly: Native API Reference

A consolidated summary of Doctly's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.doctly.ai/api-reference/introduction
- **API base URL:** `https://api.doctly.ai/api/v1`

## Authentication

### API Key

Authenticate with a Doctly API key from Settings -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.doctly.ai/api-reference/authentication)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `skip` in the query string as the record offset.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:id` | [docs](https://docs.doctly.ai/api-reference/documents/delete) |
| [Delete Extractor](actions/delete-extractor.md) | `DELETE /e/:extractorId` | [docs](https://docs.doctly.ai/api-reference/extractors/delete) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://docs.doctly.ai/api-reference/documents/get) |
| [Get Extractor](actions/get-extractor.md) | `GET /e/:extractorId` | [docs](https://docs.doctly.ai/api-reference/extractors/get) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.doctly.ai/api-reference/documents/list) |
| [List Extractors](actions/list-extractors.md) | `GET /e` | [docs](https://docs.doctly.ai/api-reference/extractors/list) |
| [Process Document](actions/process-document.md) | `POST /documents` | [docs](https://docs.doctly.ai/api-reference/documents/process) |
| [Run Extractor](actions/run-extractor.md) | `POST /e/:slug` | [docs](https://docs.doctly.ai/api-reference/extractors/run) |
| [Update Extractor](actions/update-extractor.md) | `PUT /e/:extractorId` | [docs](https://docs.doctly.ai/api-reference/extractors/update) |

# Happy SMS: Native API Reference

A consolidated summary of Happy SMS's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.happy.nc/docs/sms.html
- **OpenAPI specification:** https://www.happy.nc/v3/api-docs/SMS
- **API base URL:** `https://www.api.nc`

## Authentication

### X-API-KEY

Authenticate Happy SMS requests by sending the tenant API key in the X-API-KEY header on every request.

### Credentials

- **API Key:** `apiKey` · required · Happy SMS API key sent on every request as the X-API-KEY header.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://www.happy.nc/docs/sms.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; minimum 1). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Multiple sort fields can be combined.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /api/v1/protected/domain/custom-data/documents` | [docs](https://www.happy.nc/docs/sms.html) |
| [Create Documents Batch](actions/create-documents-batch.md) | `POST /api/v1/protected/domain/custom-data/bulk/documents` | [docs](https://www.happy.nc/docs/sms.html) |
| [Create Message](actions/create-message.md) | `POST /api/v1/protected/domain/sms/messages` | [docs](https://www.happy.nc/docs/sms.html) |
| [Create Messages Batch](actions/create-messages-batch.md) | `POST /api/v1/protected/domain/sms/bulk/messages` | [docs](https://www.happy.nc/docs/sms.html) |
| [Delete Document](actions/delete-document.md) | `DELETE /api/v1/protected/domain/custom-data/documents/:id` | [docs](https://www.happy.nc/docs/sms.html) |
| [Delete Documents Batch](actions/delete-documents-batch.md) | `DELETE /api/v1/protected/domain/custom-data/bulk/documents` | [docs](https://www.happy.nc/docs/sms.html) |
| [Delete Message](actions/delete-message.md) | `DELETE /api/v1/protected/domain/sms/messages/:id` | [docs](https://www.happy.nc/docs/sms.html) |
| [Delete Messages Batch](actions/delete-messages-batch.md) | `DELETE /api/v1/protected/domain/sms/bulk/messages` | [docs](https://www.happy.nc/docs/sms.html) |
| [Get Balance](actions/get-balance.md) | `GET /api/v1/protected/domain/account/ledgers/balance` | [docs](https://www.happy.nc/docs/sms.html) |
| [Get Document](actions/get-document.md) | `GET /api/v1/protected/domain/custom-data/documents/:id` | [docs](https://www.happy.nc/docs/sms.html) |
| [Get Message](actions/get-message.md) | `GET /api/v1/protected/domain/sms/messages/:id` | [docs](https://www.happy.nc/docs/sms.html) |
| [List Documents](actions/list-documents.md) | `GET /api/v1/protected/domain/custom-data/documents` | [docs](https://www.happy.nc/docs/sms.html) |
| [List Messages](actions/list-messages.md) | `GET /api/v1/protected/domain/sms/messages` | [docs](https://www.happy.nc/docs/sms.html) |
| [Pop Messages](actions/pop-messages.md) | `GET /api/v1/protected/domain/sms/messages/pop` | [docs](https://www.happy.nc/docs/sms.html) |
| [Search Messages](actions/search-messages.md) | `GET /api/v1/protected/domain/sms/messages/lookup` | [docs](https://www.happy.nc/docs/sms.html) |
| [Update Document](actions/update-document.md) | `PUT /api/v1/protected/domain/custom-data/documents/:id` | [docs](https://www.happy.nc/docs/sms.html) |

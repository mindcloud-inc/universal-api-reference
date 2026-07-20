# DocDroid: Native API Reference

A consolidated summary of DocDroid's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://www.docdroid.com/apidocs
- **OpenAPI specification:** https://www.docdroid.com/api/docs?api-docs.json
- **API base URL:** `https://www.docdroid.com/api`

## Authentication

### API Key

Use a DocDroid personal access token as a bearer token for the DocDroid REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.docdroid.com/apidocs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.lastPage`. The current page number is read from `meta.currentPage`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook` | [docs](https://www.docdroid.com/apidocs) |
| [Delete Document](actions/delete-document.md) | `DELETE /document/:id` | [docs](https://www.docdroid.com/apidocs) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/:id` | [docs](https://www.docdroid.com/apidocs) |
| [Get Document](actions/get-document.md) | `GET /document/:id` | [docs](https://www.docdroid.com/apidocs) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhook/:id` | [docs](https://www.docdroid.com/apidocs) |
| [List My Documents](actions/list-my-documents.md) | `GET /document` | [docs](https://www.docdroid.com/apidocs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhook` | [docs](https://www.docdroid.com/apidocs) |
| [Update Document](actions/update-document.md) | `PUT /document/:id` | [docs](https://www.docdroid.com/apidocs) |
| [Upload Document](actions/upload-document.md) | `POST /document` | [docs](https://www.docdroid.com/apidocs) |

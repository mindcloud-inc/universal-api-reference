# Charla: Native API Reference

A consolidated summary of Charla's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://charla.com/public-api.html
- **OpenAPI specification:** https://app.charla.com/swagger/v1/swagger.json
- **API base URL:** `https://api.charla.com/v1`

## Authentication

### API Key

Authenticate with a Charla API key sent in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://charla.com/support/?article=23477-rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `paging.next_cursor`.

## Pagination

Use `cursor` in the query string as the record offset; numbering starts at 0.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Article](actions/delete-article.md) | `DELETE /kb/article/:id` | [docs](https://charla.com/public-api.html) |
| [Get Article](actions/get-article.md) | `GET /kb/articles/:id` | [docs](https://charla.com/public-api.html) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://charla.com/public-api.html) |
| [List Articles](actions/list-articles.md) | `GET /kb/articles` | [docs](https://charla.com/public-api.html) |
| [List Categories](actions/list-categories.md) | `GET /kb/categories` | [docs](https://charla.com/public-api.html) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://charla.com/public-api.html) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://charla.com/public-api.html) |
| [Save Article](actions/save-article.md) | `POST /kb/articles` | [docs](https://charla.com/public-api.html) |
| [Save Contact](actions/save-contact.md) | `POST /contacts` | [docs](https://charla.com/public-api.html) |

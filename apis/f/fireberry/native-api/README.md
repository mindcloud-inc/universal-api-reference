# Fireberry: Native API Reference

A consolidated summary of Fireberry's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developers.fireberry.com/reference
- **API base URL:** `https://api.fireberry.com`

## Authentication

### API Key

Use your Fireberry API token. It will be sent as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
tokenid: <apiKey>
```

[Official authentication documentation](https://developers.fireberry.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `data.pageNumber`.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | `GET /api/record/contact` | [docs](https://developers.fireberry.com/reference/get-all-contacts) |

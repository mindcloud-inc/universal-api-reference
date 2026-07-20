# Fairing: Native API Reference

A consolidated summary of Fairing's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.fairing.co/reference/api
- **API base URL:** `https://app.fairing.co/api`

## Authentication

### API Key

Use a Fairing API key from your Fairing Settings tab to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.fairing.co/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 2; maximum 100).

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Questions](actions/list-questions.md) | `GET /questions` | [docs](https://docs.fairing.co/reference/retrieve-questions) |
| [List Responses](actions/list-responses.md) | `GET /responses` | [docs](https://docs.fairing.co/reference/retrieve-responses) |

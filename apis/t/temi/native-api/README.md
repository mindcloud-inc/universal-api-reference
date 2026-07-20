# Temi: Native API Reference

A consolidated summary of Temi's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.temi.com/api/reference/v1
- **API base URL:** `https://api.temi.com/v1`

## Authentication

### API key

Authenticate Temi API requests with a Bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.temi.com/api/reference/v1)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://www.temi.com/api/reference/v1) |
| [Delete Job](actions/delete-job.md) | `DELETE /jobs/:id` | [docs](https://www.temi.com/api/reference/v1) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://www.temi.com/api/reference/v1) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://www.temi.com/api/reference/v1) |
| [Share Transcript Editor URL](actions/share-transcript-editor-url.md) | `POST /jobs/:id/share` | [docs](https://www.temi.com/api/reference/v1) |

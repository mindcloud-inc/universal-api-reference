# Tailwind: Native API Reference

A consolidated summary of Tailwind's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.tailwind.ai/getting-started/
- **API base URL:** `https://api-v1.tailwind.ai`

## Authentication

### API Key

Create an API key in Tailwind, then use it as the app test connection and agent connection. Tailwind's REST API expects Authorization: Bearer <API key>. Do not create duplicate auth fields; the platform's implicit credentials.apiKey contract is the source of truth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-docs.tailwind.ai/getting-started/authentication)

## API conventions

The next-page cursor is read from `data.cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | `POST /v1/accounts/:accountId/posts` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidposts/post) |
| [Delete Post](actions/delete-post.md) | `DELETE /v1/accounts/:accountId/posts/:postId` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidpostspostid/delete) |
| [Get Post](actions/get-post.md) | `GET /v1/accounts/:accountId/posts/:postId` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidpostspostid/get) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://api-docs.tailwind.ai/rest-api/operations/health) |
| [List Accounts](actions/list-accounts.md) | `GET /v1/accounts` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accounts) |
| [List Board Lists](actions/list-board-lists.md) | `GET /v1/accounts/:accountId/board-lists` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidboard-lists) |
| [List Boards](actions/list-boards.md) | `GET /v1/accounts/:accountId/boards` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidboards) |
| [List Posts](actions/list-posts.md) | `GET /v1/accounts/:accountId/posts` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidposts/get) |
| [List Timeslots](actions/list-timeslots.md) | `GET /v1/accounts/:accountId/timeslots` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidtimeslots) |
| [Schedule Post](actions/schedule-post.md) | `POST /v1/accounts/:accountId/posts/:postId/schedule` | [docs](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidpostspostidschedule) |

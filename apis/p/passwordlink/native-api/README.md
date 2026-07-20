# Password.link: Native API Reference

A consolidated summary of Password.link's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://password.link/en/p/docs/api
- **API base URL:** `https://password.link/api`

## Authentication

### Private API Key

Use the private API key for normal REST actions: create, list, and delete secrets plus secret requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://password.link/en/p/docs/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Secret](actions/create-secret.md) | `POST /secrets` | [docs](https://password.link/en/p/docs/api) |
| [Create Secret Request](actions/create-secret-request.md) | `POST /secret_requests` | [docs](https://password.link/en/p/docs/api) |
| [Delete Secret](actions/delete-secret.md) | `DELETE /secrets/:id` | [docs](https://password.link/en/p/docs/api) |
| [Delete Secret Request](actions/delete-secret-request.md) | `DELETE /secret_requests/:id` | [docs](https://password.link/en/p/docs/api) |
| [List Secret Requests](actions/list-secret-requests.md) | `GET /secret_requests` | [docs](https://password.link/en/p/docs/api) |
| [List Secrets](actions/list-secrets.md) | `GET /secrets` | [docs](https://password.link/en/p/docs/api) |
| [View Secret](actions/view-secret.md) | `GET /secrets/:id` | [docs](https://password.link/en/p/docs/api) |

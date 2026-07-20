# Linear: Native API Reference

A consolidated summary of Linear's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://linear.app/developers
- **REST base URL:** `https://api.linear.app/graphql/`
- **GraphQL base URL:** `https://api.linear.app/graphql/`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://linear.app/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.linear.app/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write admin`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.linear.app/oauth/token.

[Official authentication documentation](https://linear.app/developers/oauth-2-0-authentication)

### API Token

Use a personal Linear API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://linear.app/docs/security-and-access)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `pageInfo.endCursor`.

### GraphQL

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `pageInfo.endCursor`.

## Pagination

- **REST:** Use `limit` in the request parameters to set the page size (default 50; accepted range 1–250). Use `cursor` in the request parameters as the pagination cursor.
- **GraphQL:** Use `limit` in the request parameters to set the page size (default 50; accepted range 1–250). Use `cursor` in the request parameters as the pagination cursor.

## Filtering

- **REST:** Send filters in the request body.
- **GraphQL:** Send filters in the request body.

## Sorting

- **REST:** Send sorting in the request body. Only one sort field is accepted.
- **GraphQL:** Send sorting in the request body. Only one sort field is accepted.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | `POST` | [docs](https://linear.app/developers/graphql#queries-and-mutations) |
| [Get User](actions/get-user.md) | `POST` | [docs](https://linear.app/developers/graphql#queries-and-mutations) |
| [List Issues](actions/list-issues.md) | `POST` | [docs](https://linear.app/developers/graphql#queries-and-mutations) |
| [List Teams](actions/list-teams.md) | `POST` | [docs](https://linear.app/developers/graphql#queries-and-mutations) |
| [Query](actions/query.md) | `POST` | [docs](https://linear.app/developers/graphql#queries-and-mutations) |
| [Update Issue](actions/update-issue.md) | `POST` | [docs](https://linear.app/developers/graphql#queries-and-mutations) |

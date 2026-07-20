# Reflect: Native API Reference

A consolidated summary of Reflect's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://reflect.academy/api
- **OpenAPI specification:** https://openpm.ai/packages/reflect/openapi.json
- **API base URL:** `https://reflect.app/api`

## Authentication

### OAuth2

Connect Reflect with OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://reflect.app/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://reflect.app/api/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read:graph write:graph`.

[Official authentication documentation](https://reflect.app/developer/oauth)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append to Daily Note](actions/append-to-daily-note.md) | `PUT /graphs/:graphId/daily-notes` | [docs](https://openpm.ai/packages/reflect#/graphs/{graphId}/daily-notes) |
| [Create Link](actions/create-link.md) | `POST /graphs/:graphId/links` | [docs](https://openpm.ai/packages/reflect#/graphs/{graphId}/links) |
| [Create Note](actions/create-note.md) | `POST /graphs/:graphId/notes` | [docs](https://openpm.ai/packages/reflect#/graphs/{graphId}/notes) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://openpm.ai/packages/reflect#/users/me) |
| [List Books](actions/list-books.md) | `GET /graphs/:graphId/books` | [docs](https://openpm.ai/packages/reflect#/graphs/{graphId}/books) |
| [List Graphs](actions/list-graphs.md) | `GET /graphs` | [docs](https://openpm.ai/packages/reflect#/graphs) |
| [List Links](actions/list-links.md) | `GET /graphs/:graphId/links` | [docs](https://openpm.ai/packages/reflect#/graphs/{graphId}/links) |

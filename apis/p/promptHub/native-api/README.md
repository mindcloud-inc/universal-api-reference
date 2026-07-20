# PromptHub: Native API Reference

A consolidated summary of PromptHub's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation
- **API base URL:** `https://app.prompthub.us/api/v1`

## Authentication

### API Key

Authenticate PromptHub API requests with a bearer API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /me` | [docs](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation) |
| [Get Project Head](actions/get-project-head.md) | `GET /projects/:projectId/head` | [docs](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation) |
| [List Projects](actions/list-projects.md) | `GET /teams/:teamId/projects` | [docs](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation) |
| [Run Project](actions/run-project.md) | `POST /projects/:projectId/run` | [docs](https://intercom.help/prompthub/en/articles/8541389-prompthub-api-documentation) |

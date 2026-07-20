# v0: Native API Reference

A consolidated summary of v0's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://v0.app/docs/api/platform/overview
- **API base URL:** `https://api.v0.dev`

## Authentication

### API Key

Authenticate with a v0 Platform API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://v0.app/docs/api/platform/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat](actions/create-chat.md) | `POST /v1/chats` | [docs](https://v0.app/docs/api/platform/reference/chats/create) |
| [Create Deployment](actions/create-deployment.md) | `POST /v1/deployments` | [docs](https://v0.app/docs/api/platform/reference/deployments/create) |
| [Create Environment Variables](actions/create-environment-variables.md) | `POST /v1/projects/:projectId/env-vars` | [docs](https://v0.app/docs/api/platform/reference/projects/create-env-vars) |
| [Create Project](actions/create-project.md) | `POST /v1/projects` | [docs](https://v0.app/docs/api/platform/reference/projects/create) |
| [Find Chat Messages](actions/find-chat-messages.md) | `GET /v1/chats/:chatId/messages` | [docs](https://v0.app/docs/api/platform/reference/chats/find-messages) |
| [Find Chat Versions](actions/find-chat-versions.md) | `GET /v1/chats/:chatId/versions` | [docs](https://v0.app/docs/api/platform/reference/chats/find-versions) |
| [Find Chats](actions/find-chats.md) | `GET /v1/chats` | [docs](https://v0.app/docs/api/platform/reference/chats/find) |
| [Find Deployment Logs](actions/find-deployment-logs.md) | `GET /v1/deployments/:deploymentId/logs` | [docs](https://v0.app/docs/api/platform/reference/deployments/find-logs) |
| [Find Deployments](actions/find-deployments.md) | `GET /v1/deployments` | [docs](https://v0.app/docs/api/platform/reference/deployments/find) |
| [Find Environment Variables](actions/find-environment-variables.md) | `GET /v1/projects/:projectId/env-vars` | [docs](https://v0.app/docs/api/platform/reference/projects/find-env-vars) |
| [Find Projects](actions/find-projects.md) | `GET /v1/projects` | [docs](https://v0.app/docs/api/platform/reference/projects/find) |
| [Find Rate Limit](actions/find-rate-limit.md) | `GET /v1/rate-limits` | [docs](https://v0.app/docs/api/platform/reference/rate-limits/find) |
| [Get Billing](actions/get-billing.md) | `GET /v1/user/billing` | [docs](https://v0.app/docs/api/platform/reference/user/get-billing) |
| [Get Chat](actions/get-chat.md) | `GET /v1/chats/:chatId` | [docs](https://v0.app/docs/api/platform/reference/chats/get-by-id) |
| [Get Chat Version](actions/get-chat-version.md) | `GET /v1/chats/:chatId/versions/:versionId` | [docs](https://v0.app/docs/api/platform/reference/chats/get-version) |
| [Get Plan](actions/get-plan.md) | `GET /v1/user/plan` | [docs](https://v0.app/docs/api/platform/reference/user/get-plan) |
| [Get Project by ID](actions/get-project-by-id.md) | `GET /v1/projects/:projectId` | [docs](https://v0.app/docs/api/platform/reference/projects/get-by-id) |
| [Get User](actions/get-user.md) | `GET /v1/user` | [docs](https://v0.app/docs/api/platform/reference/user/get) |
| [Get User Scopes](actions/get-user-scopes.md) | `GET /v1/user/scopes` | [docs](https://v0.app/docs/api/platform/reference/user/get-scopes) |
| [Initialize Chat](actions/initialize-chat.md) | `POST /v1/chats/init` | [docs](https://v0.app/docs/api/platform/reference/chats/init) |
| [Send Message](actions/send-message.md) | `POST /v1/chats/:chatId/messages` | [docs](https://v0.app/docs/api/platform/reference/chats/send-message) |
| [Update Chat](actions/update-chat.md) | `PATCH /v1/chats/:chatId` | [docs](https://v0.app/docs/api/platform/reference/chats/update) |
| [Update Environment Variables](actions/update-environment-variables.md) | `PATCH /v1/projects/:projectId/env-vars` | [docs](https://v0.app/docs/api/platform/reference/projects/update-env-vars) |
| [Update Project](actions/update-project.md) | `PATCH /v1/projects/:projectId` | [docs](https://v0.app/docs/api/platform/reference/projects/update) |

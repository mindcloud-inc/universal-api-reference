# Superglue: Native API Reference

A consolidated summary of Superglue's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.superglue.cloud/api-reference
- **OpenAPI specification:** https://docs.superglue.cloud/openapi.yaml
- **API base URL:** `https://api.superglue.ai/v1`

## Authentication

### API Key

Authenticate Superglue API requests with a static bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.superglue.cloud/guides/secure-gateway)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 50; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | `POST /runs/:runId/cancel` | [docs](https://docs.superglue.cloud/api-reference/runs/cancel-a-run) |
| [Create End User](actions/create-end-user.md) | `POST /end-users` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/create-end-user) |
| [Delete End User](actions/delete-end-user.md) | `DELETE /end-users/:endUserId` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/delete-end-user) |
| [Generate Portal Link](actions/generate-portal-link.md) | `POST /end-users/:endUserId/portal-token` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/generate-portal-link) |
| [Get End User Details](actions/get-end-user-details.md) | `GET /end-users/:endUserId` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/get-end-user-details) |
| [Get Full Run Results](actions/get-full-run-results.md) | `GET /runs/:runId/results` | [docs](https://docs.superglue.cloud/api-reference/runs/get-full-run-results) |
| [Get Run Status and Metadata](actions/get-run-status-and-metadata.md) | `GET /runs/:runId` | [docs](https://docs.superglue.cloud/api-reference/runs/get-run-status-and-metadata) |
| [Get Tool Details](actions/get-tool-details.md) | `GET /tools/:toolId` | [docs](https://docs.superglue.cloud/api-reference/tools/get-tool-details) |
| [List End Users](actions/list-end-users.md) | `GET /end-users` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/list-end-users) |
| [List Runs](actions/list-runs.md) | `GET /runs` | [docs](https://docs.superglue.cloud/api-reference/runs/list-runs) |
| [List Tools](actions/list-tools.md) | `GET /tools` | [docs](https://docs.superglue.cloud/api-reference/tools/list-tools) |
| [Run Tool](actions/run-tool.md) | `POST /tools/:toolId/run` | [docs](https://docs.superglue.cloud/api-reference/tools/run-a-tool) |
| [Send Portal Invitation Email](actions/send-portal-invitation-email.md) | `POST /end-users/:endUserId/invite` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/send-portal-invitation-email) |
| [Update End User](actions/update-end-user.md) | `PATCH /end-users/:endUserId` | [docs](https://docs.superglue.cloud/api-reference/end-users-enterprise/update-end-user) |

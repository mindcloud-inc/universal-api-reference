# Tinq.ai: Native API Reference

A consolidated summary of Tinq.ai's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.tinq.ai/api-reference
- **API base URL:** `https://tinq.ai`

## Authentication

### API Key

Use a Tinq.ai API token and workspace UUID.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · Tinq workspace UUID used by workspace-scoped routes.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.tinq.ai/api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Documents](actions/delete-documents.md) | `DELETE /api/v2/documents/delete` | [docs](https://docs.tinq.ai/api-reference) |
| [Enhance Prompt](actions/enhance-prompt.md) | `POST /api/v2/enhance-prompt` | [docs](https://docs.tinq.ai/api-reference) |
| [Get Datasource](actions/get-datasource.md) | `GET /api/v2/datasources/:workspaceId/:datasourceId` | [docs](https://docs.tinq.ai/api-reference) |
| [Get Document](actions/get-document.md) | `GET /api/v2/documents/:slug` | [docs](https://docs.tinq.ai/api-reference) |
| [Get Task Status](actions/get-task-status.md) | `GET /api/v2/tasks/:taskId` | [docs](https://docs.tinq.ai/api-reference) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/v2/workspaces/:uuid` | [docs](https://docs.tinq.ai/api-reference) |
| [List Activities](actions/list-activities.md) | `GET /api/v2/activities-log` | [docs](https://docs.tinq.ai/api-reference) |
| [List Datasource Documents](actions/list-datasource-documents.md) | `GET /api/v2/datasources/documents` | [docs](https://docs.tinq.ai/api-reference) |
| [List Datasources](actions/list-datasources.md) | `GET /api/v2/datasources/:workspaceId` | [docs](https://docs.tinq.ai/api-reference) |
| [List Documents](actions/list-documents.md) | `GET /api/v2/documents` | [docs](https://docs.tinq.ai/api-reference) |
| [List Models](actions/list-models.md) | `GET /api/v2/models` | [docs](https://docs.tinq.ai/api-reference) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v2/tasks` | [docs](https://docs.tinq.ai/api-reference) |
| [Rewrite Text](actions/rewrite-text.md) | `POST /api/v2/rewrite` | [docs](https://docs.tinq.ai/api-reference) |
| [Search Workspace](actions/search-workspace.md) | `POST /api/v2/search` | [docs](https://docs.tinq.ai/api-reference) |
| [Sync Datasource Documents](actions/sync-datasource-documents.md) | `POST /api/v2/datasources/sync/:workspaceId` | [docs](https://docs.tinq.ai/api-reference) |

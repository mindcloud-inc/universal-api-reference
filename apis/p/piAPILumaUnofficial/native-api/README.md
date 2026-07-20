# PiAPI/Luma (unofficial): Native API Reference

A consolidated summary of PiAPI/Luma (unofficial)'s API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/doc-678694
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Authenticate with a PiAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://piapi.ai/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `data.page`.

## Pagination

Use `page_size` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Luma Task](actions/cancel-luma-task.md) | `DELETE /api/v1/task/:task_id` | [docs](https://piapi.ai/docs/dream-machine/cancel-task) |
| [Cancel Luma Tasks](actions/cancel-luma-tasks.md) | `DELETE /api/v1/tasks` | [docs](https://piapi.ai/docs/dream-machine/cancel-tasks) |
| [Create Luma Task](actions/create-luma-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/dream-machine/create-task) |
| [Get Luma Task](actions/get-luma-task.md) | `GET /api/v1/task/:task_id` | [docs](https://piapi.ai/docs/dream-machine/get-task) |
| [Get PiAPI Account Info](actions/get-piapi-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get PiAPI Active Tasks](actions/list-piapi-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List PiAPI Luma Task History](actions/list-piapi-luma-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

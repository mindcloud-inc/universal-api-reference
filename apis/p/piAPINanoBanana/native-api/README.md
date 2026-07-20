# PiAPI/NanoBanana: Native API Reference

A consolidated summary of PiAPI/NanoBanana's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/quickstart
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

PiAPI requires the workspace API key to be sent on each request in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://piapi.ai/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Gemini 2.5 Flash Image Task](actions/create-gemini25-flash-image-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/gemini-api/gemini-25-flash-image) |
| [Create Nano Banana Pro Task](actions/create-nano-banana-pro-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/gemini-api/nano-banana-pro) |
| [Create Nano Banana 2 Task](actions/create-nano-banana2-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/gemini-api/nano-banana-2) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/gemini-api/get-task) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List User Task History](actions/list-user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

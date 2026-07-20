# PiAPI/Skyreels: Native API Reference

A consolidated summary of PiAPI/Skyreels's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/overview
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Connect PiAPI using an API key from PiAPI Workspace.

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

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Skyreels Task](actions/create-skyreels-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/skyreels-api/create-task) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Skyreels Task](actions/get-skyreels-task.md) | `GET /api/v1/task/:task_id` | [docs](https://piapi.ai/docs/skyreels-api/get-task) |

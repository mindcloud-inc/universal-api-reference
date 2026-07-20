# PiAPI/Trellis: Native API Reference

A consolidated summary of PiAPI/Trellis's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/trellis-api/create-task
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

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Trellis Image-to-3D Task](actions/create-trellis-image-to-3d-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/trellis-api/create-task) |
| [Create Trellis Text-to-3D Task](actions/create-trellis-text-to-3d-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/trellis-api/create-task) |
| [Create Trellis2 Image-to-3D Task](actions/create-trellis2-image-to-3d-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/trellis2-api/create-task) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/:task_id` | [docs](https://piapi.ai/docs/trellis-api/get-task) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List Task History](actions/list-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

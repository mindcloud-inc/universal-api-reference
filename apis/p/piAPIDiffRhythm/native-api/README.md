# PiAPI/DiffRhythm: Native API Reference

A consolidated summary of PiAPI/DiffRhythm's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/diffrhythm-api/create-task
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Connect PiAPI with an API key from the PiAPI workspace.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://piapi.ai/docs/quickstart)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [File Upload API](actions/file-upload-api.md) | `POST https://upload.theapi.app/api/ephemeral_resource` | [docs](https://piapi.ai/docs/tools/file-upload) |
| [Generate Audio](actions/generate-audio.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/diffrhythm-api/create-task) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/diffrhythm/get-task) |
| [PiAPI Account Info](actions/piapi-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Task List Info](actions/task-list-info.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [User Task History](actions/user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

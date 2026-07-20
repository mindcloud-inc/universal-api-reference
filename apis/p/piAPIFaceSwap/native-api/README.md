# PiAPI/FaceSwap: Native API Reference

A consolidated summary of PiAPI/FaceSwap's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/doc-678694
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Authenticate with a PiAPI workspace API key.

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

Responses from this API use JSON. The current page number is read from `data.page`.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/faceswap-api/get-task) |
| [Image Faceswap](actions/image-faceswap.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/api-10275990) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List User Task History](actions/list-user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |
| [Multi Faceswap](actions/multi-faceswap.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/multi-face-swap/create-task) |
| [Video Faceswap](actions/video-faceswap.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/faceswap-api/video-faceswap) |

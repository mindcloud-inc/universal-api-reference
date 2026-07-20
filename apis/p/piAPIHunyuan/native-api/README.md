# PiAPI/Hunyuan: Native API Reference

A consolidated summary of PiAPI/Hunyuan's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/hunyuan-video/txt2video-api
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Authenticate with your PiAPI API key.

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

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Fast Text to Video Task](actions/create-fast-text-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/hunyuan-video/txt2video-api) |
| [Create Image to Video (Concat) Task](actions/create-image-to-video-concat-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/hunyuan-video/txt2video-api) |
| [Create Image to Video (Replace) Task](actions/create-image-to-video-replace-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/hunyuan-video/txt2video-api) |
| [Create Text to Video Task](actions/create-text-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/hunyuan-video/txt2video-api) |
| [Create Text to Video with LoRA Task](actions/create-text-to-video-with-lo-ra-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/hunyuan-api-doc) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/:taskId` | [docs](https://piapi.ai/docs/hunyuan-api/get-task) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List User Task History](actions/list-user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

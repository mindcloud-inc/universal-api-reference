# PiAPI/Toolkit: Native API Reference

A consolidated summary of PiAPI/Toolkit's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/endpoints
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

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

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [File Upload API](actions/file-upload-api.md) | `POST https://upload.theapi.app/api/ephemeral_resource` | [docs](https://piapi.ai/docs/tools/file-upload) |
| [Image Upscale - Get Task](actions/image-upscale-get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/image-upscale/get-task) |
| [Image Upscale (Super Resolution) API](actions/image-upscale-super-resolution.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/image-editing-api/super-resolution-api) |
| [PiAPI Account Info](actions/piapi-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Remove Background API](actions/remove-background.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/image-editing-api/remove-background-api) |
| [Remove Background - Get Task](actions/remove-background-get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/remove-background/get-task) |
| [Segment With Prompt API](actions/segment-with-prompt.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/image-editing-api/segment-with-prompt-api) |
| [Segment With Prompt - Get Task](actions/segment-with-prompt-get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/segment-with-prompt/get-task) |
| [Task List Info](actions/task-list-info.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [User Task History](actions/user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |
| [Video Remove Background](actions/video-remove-background.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/tools/video-remove-background-api) |
| [Video Remove Background - Get Task](actions/video-remove-background-get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/video-remove-background/get-scale) |
| [Video Upscale](actions/video-upscale.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/tools/video-upscale-api) |
| [Video Upscale - Get Task](actions/video-upscale-get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/video-upscale/get-scale) |

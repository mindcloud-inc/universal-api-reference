# PiAPI/Kling: Native API Reference

A consolidated summary of PiAPI/Kling's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/kling-api/create-task
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Authenticate PiAPI Kling requests with your PiAPI API key.

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

Use `page_size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Task](actions/cancel-task.md) | `DELETE /api/v1/task/:task_id` | [docs](https://piapi.ai/docs/kling-api/cancel-task) |
| [Cancel Tasks Before Timestamp](actions/cancel-tasks-before-timestamp.md) | `DELETE /api/v1/tasks` | [docs](https://piapi.ai/docs/kling-api/cancel-tasks) |
| [Generate Avatar Video](actions/generate-avatar-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-avatar-api) |
| [Generate Effects Video](actions/generate-effects-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-effects-api) |
| [Generate Elements Video](actions/generate-elements-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-elements) |
| [Generate Motion Control Video](actions/generate-motion-control-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-motion-control-api) |
| [Generate Omni Video](actions/generate-omni-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-3-omni-api) |
| [Generate Sound](actions/generate-sound.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-sound-api) |
| [Generate Turbo Video](actions/generate-turbo-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/kling-turbo-api) |
| [Generate Video from Image](actions/generate-video-from-image.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/create-task) |
| [Generate Video from Text](actions/generate-video-from-text.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/create-task) |
| [Generate Virtual Try-On](actions/generate-virtual-try-on.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/virtual-try-on-api) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/:task_id` | [docs](https://piapi.ai/docs/kling-api/get-task) |
| [Lip Sync Video](actions/lip-sync-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/kling-api/lipsync-examples) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List User Task History](actions/list-user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

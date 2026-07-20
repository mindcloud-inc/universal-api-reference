# PiAPI/Veo: Native API Reference

A consolidated summary of PiAPI/Veo's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/doc-678694
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Authenticate PiAPI requests with your API key.

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

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Veo3 Image to Video Task](actions/create-veo3-image-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/veo3-api/image-to-video) |
| [Create Veo3 Text to Video Task](actions/create-veo3-text-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/veo3-api/text-to-video) |
| [Create Veo3.1 Image to Video Task](actions/create-veo31-image-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/veo31-api/image-to-video) |
| [Create Veo3.1 Text to Video Task](actions/create-veo31-text-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/veo31-api/text-to-video) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/:taskId` | [docs](https://piapi.ai/docs/veo3-api/get-task) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List User Task History](actions/list-user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

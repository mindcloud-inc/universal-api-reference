# DomoAI: Native API Reference

A consolidated summary of DomoAI's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.domoai.app/api-reference/introduction
- **API base URL:** `https://api.domoai.com`

## Authentication

### API Key

Use a DomoAI Enterprise API key as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.domoai.app/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Image to Video Task](actions/create-image-to-video-task.md) | `POST /v1/video/image2video` | [docs](https://docs.domoai.app/api-reference/ai-video/image-to-video) |
| [Create Talking Avatar Task](actions/create-talking-avatar-task.md) | `POST /v1/video/talking-avatar` | [docs](https://docs.domoai.app/api-reference/ai-video/talking-avatar) |
| [Create Template to Video Task](actions/create-template-to-video-task.md) | `POST /v1/video/template2video` | [docs](https://docs.domoai.app/api-reference/ai-video/template-to-video) |
| [Create Text to Video Task](actions/create-text-to-video-task.md) | `POST /v1/video/text2video` | [docs](https://docs.domoai.app/api-reference/ai-video/text-to-video) |
| [Create Video to Video Task](actions/create-video-to-video-task.md) | `POST /v1/video/video2video` | [docs](https://docs.domoai.app/api-reference/ai-video/video-to-video) |
| [Get Task](actions/get-task.md) | `GET /v1/tasks/[:taskId]` | [docs](https://docs.domoai.app/api-reference/task/get-task) |
| [Upload File](actions/upload-file.md) | `POST /v1/upload/file` | [docs](https://docs.domoai.app/api-reference/upload/upload-file) |

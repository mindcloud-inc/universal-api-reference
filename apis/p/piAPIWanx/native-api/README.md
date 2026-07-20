# PiAPI/Wanx: Native API Reference

A consolidated summary of PiAPI/Wanx's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/wanx-api/create-task
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

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Image to Video with Camera Control](actions/create-image-to-video-control-camera.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Image to Video with Keyframes](actions/create-image-to-video-keyframe.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Image to Video (Wan 2.2)](actions/create-image-to-video-wan22.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Image to Video (14B)](actions/create-image-to-video14b.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Image to Video with LoRA](actions/create-image-to-video14b-lora.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Text to Video (Wan 2.2)](actions/create-text-to-video-wan22.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Text to Video (1.3B)](actions/create-text-to-video13b.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Text to Video (14B)](actions/create-text-to-video14b.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Create Text to Video with LoRA](actions/create-text-to-video14b-lora.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/wanx-api/create-task) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/[:task_id]` | [docs](https://piapi.ai/docs/wanx-api/get-task) |

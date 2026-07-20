# PiAPI/Sora: Native API Reference

A consolidated summary of PiAPI/Sora's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/sora2-api/text-to-video
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

Response data is read from `data`.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Sora2 Pro Text to Video Task](actions/create-sora2-pro-text-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/sora2-pro-api/text-to-video) |
| [Create Sora2 Text to Video Task](actions/create-sora2-text-to-video-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/sora2-api/text-to-video) |
| [Get PiAPI Account Info](actions/get-piapi-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Sora2 Task](actions/get-sora2-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/sora2-api/get-task) |
| [Remove Watermark from Sora2 Video](actions/remove-watermark-from-sora2-video.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/sora2-api/remove-watermark) |

# PiAPI/Flux.1: Native API Reference

A consolidated summary of PiAPI/Flux.1's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/endpoints
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

PiAPI requires the workspace API key to be sent on each request in the x-api-key header.

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

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Flux ControlNet LoRA Task](actions/create-flux-control-net-lo-ra-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-with-lora-and-controlnet) |
| [Create Flux Fill Inpaint Task](actions/create-flux-fill-inpaint-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-redux-fill-variation-inpaint-outpaint) |
| [Create Flux Fill Outpaint Task](actions/create-flux-fill-outpaint-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-redux-fill-variation-inpaint-outpaint) |
| [Create Flux Image to Image LoRA Task](actions/create-flux-image-to-image-lo-ra-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-with-lora-and-controlnet) |
| [Create Flux Image to Image Task](actions/create-flux-image-to-image-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-api/image-to-image) |
| [Create Flux Kontext Task](actions/create-flux-kontext-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-api/kontext) |
| [Create Flux Redux Variation Task](actions/create-flux-redux-variation-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-redux-fill-variation-inpaint-outpaint) |
| [Create Flux Text to Image LoRA Task](actions/create-flux-text-to-image-lo-ra-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-with-lora-and-controlnet) |
| [Create Flux Text to Image Task](actions/create-flux-text-to-image-task.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/flux-api/text-to-image) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/info` | [docs](https://piapi.ai/docs/account-info-api) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/flux-api/get-task) |
| [List Active Tasks](actions/list-active-tasks.md) | `GET /account/active_tasks` | [docs](https://piapi.ai/docs/task-list-api) |
| [List User Task History](actions/list-user-task-history.md) | `GET /api/open/tasks/histories` | [docs](https://piapi.ai/docs/piapi-user-history-query) |

# Claid AI: Native API Reference

A consolidated summary of Claid AI's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.claid.ai
- **OpenAPI specification:** https://api.claid.ai/openapi.json
- **API base URL:** `https://api.claid.ai/v1`

## Authentication

### API Key

Connect with a Claid API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.claid.ai/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Scene](actions/create-scene.md) | `POST scene/create` | [docs](https://docs.claid.ai/ai-background-api/api-reference) |
| [Create Storage](actions/create-storage.md) | `POST storage/storages` | [docs](https://docs.claid.ai/storage-connectors/api-reference) |
| [Delete Storage](actions/delete-storage.md) | `DELETE storage/storages/:storage_id` | [docs](https://docs.claid.ai/storage-connectors/api-reference) |
| [Edit Image](actions/edit-image.md) | `POST image/edit` | [docs](https://docs.claid.ai/image-editing-api/api-reference) |
| [Generate Image](actions/generate-image.md) | `POST image/generate` | [docs](https://docs.claid.ai/image-generation-api/api-reference) |
| [Get AI Edit Generation Result](actions/get-ai-edit-generation-result.md) | `GET image/ai-edit/:ai_edit_id` | [docs](https://docs.claid.ai/image-ai-edit-api/async-api-reference) |
| [Get AI Fashion Models Generation Result](actions/get-ai-fashion-models-generation-result.md) | `GET image/ai-fashion-models/:processing_request_id` | [docs](https://docs.claid.ai/ai-fashion-models-api/async-api-reference) |
| [Get Async Image Edit Result](actions/get-async-image-edit-result.md) | `GET image/edit/async/:task_id` | [docs](https://docs.claid.ai/image-editing-api/async-api-reference) |
| [Get Batch Image Edit Results](actions/get-batch-image-edit-results.md) | `GET image/edit/batch/:task_id` | [docs](https://docs.claid.ai/image-editing-api/batch-api-reference) |
| [Get Storage](actions/get-storage.md) | `GET storage/storages/:storage_id` | [docs](https://docs.claid.ai/storage-connectors/api-reference) |
| [Get Video Generation Status](actions/get-video-generation-status.md) | `GET video/generate/:animation_id` | [docs](https://docs.claid.ai/image-to-video-api/async-api-reference) |
| [List Storage Types](actions/list-storage-types.md) | `GET storage/storage-types` | [docs](https://docs.claid.ai/storage-connectors/api-reference) |
| [List Storages](actions/list-storages.md) | `GET storage/storages` | [docs](https://docs.claid.ai/storage-connectors/api-reference) |
| [Process Batch Image Edit](actions/process-batch-image-edit.md) | `POST image/edit/batch` | [docs](https://docs.claid.ai/image-editing-api/batch-api-reference) |
| [Start AI Fashion Models](actions/start-ai-fashion-models.md) | `POST image/ai-fashion-models` | [docs](https://docs.claid.ai/ai-fashion-models-api/async-api-reference) |
| [Start AI Image Edit](actions/start-ai-image-edit.md) | `POST image/ai-edit` | [docs](https://docs.claid.ai/image-ai-edit-api/async-api-reference) |
| [Start Async Image Edit](actions/start-async-image-edit.md) | `POST image/edit/async` | [docs](https://docs.claid.ai/image-editing-api/async-api-reference) |
| [Start Video Generation](actions/start-video-generation.md) | `POST video/generate` | [docs](https://docs.claid.ai/image-to-video-api/async-api-reference) |
| [Update Storage](actions/update-storage.md) | `PATCH storage/storages/:storage_id` | [docs](https://docs.claid.ai/storage-connectors/api-reference) |
| [Upload Image For Edit](actions/upload-image-for-edit.md) | `POST image/edit/upload` | [docs](https://docs.claid.ai/image-editing-api/upload-api-reference) |

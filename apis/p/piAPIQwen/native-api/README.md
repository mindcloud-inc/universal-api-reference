# PiAPI/Qwen: Native API Reference

A consolidated summary of PiAPI/Qwen's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs
- **API base URL:** `https://api.piapi.ai/api/v1`

## Authentication

### API Key

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

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Image Edit Task](actions/create-image-edit-task.md) | `POST /task` | [docs](https://piapi.ai/docs/qwen-image-api/image-edit) |
| [Create Text to Image Task](actions/create-text-to-image-task.md) | `POST /task` | [docs](https://piapi.ai/docs/qwen-image-api/text-to-image) |
| [Get Task](actions/get-task.md) | `GET /task/{task_id}` | [docs](https://piapi.ai/docs/qwen-image-api/get-task) |

# Wiro: Native API Reference

A consolidated summary of Wiro's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://wiro.ai/docs/introduction
- **API base URL:** `https://api.wiro.ai/v1`

## Authentication

### Wiro API Key

Use a Wiro tenant API key. This app is configured for the verified API-key-only x-api-key contract.

### Credentials

- **API Key:** `apiKey` · required · Your Wiro project API key. Wiro REST requests for this tenant send it as the shared x-api-key header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://wiro.ai/docs/pricing)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Task](actions/cancel-task.md) | `POST /Task/Cancel` | [docs](https://wiro.ai/docs/tasks#task-cancel) |
| [Explore Models](actions/explore-models.md) | `POST /Tool/Explore` | [docs](https://wiro.ai/docs/models) |
| [Get Model Schema](actions/get-model-schema.md) | `POST /Tool/Detail` | [docs](https://wiro.ai/docs/models#model-detail) |
| [Get Task](actions/get-task.md) | `POST /Task/Detail` | [docs](https://wiro.ai/docs/tasks#task-detail) |
| [Kill Task](actions/kill-task.md) | `POST /Task/Kill` | [docs](https://wiro.ai/docs/tasks#task-kill) |
| [Run Model](actions/run-model.md) | `POST /Run/{slugowner}/{slugproject}` | [docs](https://wiro.ai/docs/run-a-model#run-endpoint) |
| [Search Models](actions/search-models.md) | `POST /Tool/List` | [docs](https://wiro.ai/docs/models#list-models) |
| [Upload File](actions/upload-file.md) | `POST /File/Upload` | [docs](https://wiro.ai/docs/files#file-upload) |

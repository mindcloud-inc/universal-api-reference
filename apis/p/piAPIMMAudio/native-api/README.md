# PiAPI/MMAudio: Native API Reference

A consolidated summary of PiAPI/MMAudio's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://piapi.ai/docs/quickstart
- **API base URL:** `https://api.piapi.ai`

## Authentication

### API Key

Connect PiAPI with your PiAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://piapi.ai/docs/quickstart)

## API conventions

Response data is read from `data`.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Audio](actions/generate-audio.md) | `POST /api/v1/task` | [docs](https://piapi.ai/docs/mmaudio-api/create-task) |
| [Get Task](actions/get-task.md) | `GET /api/v1/task/{task_id}` | [docs](https://piapi.ai/docs/mmaudio-api/get-task) |

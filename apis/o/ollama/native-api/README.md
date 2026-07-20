# Ollama: Native API Reference

A consolidated summary of Ollama's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.ollama.com/api/introduction
- **API base URL:** `https://ollama.com`

## Authentication

### API Key

Connect to Ollama with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ollama.com/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Anthropic Message](actions/create-anthropic-message.md) | `POST /v1/messages` | [docs](https://docs.ollama.com/api/anthropic-compatibility) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.ollama.com/api/openai-compatibility) |
| [Create Response](actions/create-response.md) | `POST /v1/responses` | [docs](https://docs.ollama.com/api/openai-compatibility) |
| [Generate Chat Message](actions/generate-chat-message.md) | `POST /api/chat` | [docs](https://docs.ollama.com/api/chat) |
| [Generate Response](actions/generate-response.md) | `POST /api/generate` | [docs](https://docs.ollama.com/api/generate) |
| [Get Model (OpenAI Compatible)](actions/get-model-open-ai.md) | `GET /v1/models/:model` | [docs](https://docs.ollama.com/api/openai-compatibility) |
| [Get Version](actions/get-version.md) | `GET /api/version` | [docs](https://docs.ollama.com/api-reference/get-version) |
| [List Models](actions/list-models.md) | `GET /api/tags` | [docs](https://docs.ollama.com/api/tags) |
| [List Models (OpenAI Compatible)](actions/list-models-open-ai.md) | `GET /v1/models` | [docs](https://docs.ollama.com/api/openai-compatibility) |
| [Show Model Details](actions/show-model-details.md) | `POST /api/show` | [docs](https://docs.ollama.com/api-reference/show-model-details) |

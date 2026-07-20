# ProxyAPI: Native API Reference

A consolidated summary of ProxyAPI's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://proxyapi.ru/docs
- **API base URL:** `https://openai.api.proxyapi.ru/v1`

## Authentication

### API Key

Connect with your ProxyAPI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://proxyapi.ru/docs/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /chat/completions` | [docs](https://proxyapi.ru/docs/openai-text-generation) |
| [Custom-Tool Chat Completion](actions/custom-tool-chat-completion.md) | `POST /chat/completions` | [docs](https://platform.openai.com/docs/api-reference/chat/create) |
| [Function-Calling Chat Completion](actions/function-calling-chat-completion.md) | `POST /chat/completions` | [docs](https://platform.openai.com/docs/api-reference/chat/create) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://proxyapi.ru/docs/openai-compatible-api) |
| [Parallel Tool-Calling Chat](actions/parallel-tool-calling-chat.md) | `POST /chat/completions` | [docs](https://platform.openai.com/docs/api-reference/chat/create) |
| [Stream Chat Completion](actions/stream-chat-completion.md) | `POST /chat/completions` | [docs](https://proxyapi.ru/docs/openai-text-generation) |
| [Structured Chat Completion](actions/structured-chat-completion.md) | `POST /chat/completions` | [docs](https://platform.openai.com/docs/api-reference/chat/create) |

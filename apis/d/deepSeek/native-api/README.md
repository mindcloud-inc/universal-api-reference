# DeepSeek: Native API Reference

A consolidated summary of DeepSeek's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.deepseek.com
- **API base URL:** `https://api.deepseek.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-docs.deepseek.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /chat/completions` | [docs](https://api-docs.deepseek.com/api/create-chat-completion) |
| [Create Chat Prefix Completion (Beta)](actions/create-chat-prefix-completion-beta.md) | `POST /beta/chat/completions` | [docs](https://api-docs.deepseek.com/guides/chat_prefix_completion) |
| [Create FIM Completion (Beta)](actions/create-fim-completion-beta.md) | `POST /beta/completions` | [docs](https://api-docs.deepseek.com/api/create-completion) |
| [Get User Balance](actions/get-user-balance.md) | `GET /user/balance` | [docs](https://api-docs.deepseek.com/api/get-user-balance) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://api-docs.deepseek.com/api/list-models) |

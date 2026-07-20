# DenserChat: Native API Reference

A consolidated summary of DenserChat's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.denser.ai/docs/api/quick-start/
- **API base URL:** `https://denser.ai/api`

## Authentication

### API Key

Authenticate with a Denser API key and a connection-scoped chatbot ID.

### Credentials

- **API Key:** `apiKey` · required
- **Chatbot ID:** `chatbotId` · required · The Denser chatbot ID for the chatbot this connection should query.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.denser.ai/docs/operations/security/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Query Chatbot](actions/query-chatbot.md) | `POST /query` | [docs](https://docs.denser.ai/docs/api/chat/) |

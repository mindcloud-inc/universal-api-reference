# Alltius: Native API Reference

A consolidated summary of Alltius's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://app.alltius.ai/api/platform/documentation
- **OpenAPI specification:** https://app.alltius.ai/api/platform/openapi.json
- **API base URL:** `https://app.alltius.ai/api/platform`

## Authentication

### API Key

Connect with an Alltius API key and assistant ID

### Credentials

- **API Key:** `apiKey` · required
- **Assistant ID:** `assistantId` · required · Assistant ID for the Alltius assistant to query.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://app.alltius.ai/api/platform/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask Assistant](actions/ask-assistant.md) | `POST /v1/chat` | [docs](https://app.alltius.ai/api/platform/documentation) |
| [Delete User Chat Sessions](actions/delete-user-chat-sessions.md) | `POST /v1/chat/delete_chat_sessions_for_uid` | [docs](https://app.alltius.ai/api/platform/documentation) |
| [Get Chat History](actions/get-chat-history.md) | `POST /v1/chat/history` | [docs](https://app.alltius.ai/api/platform/documentation) |
| [Get Chat Sessions By User](actions/get-chat-sessions-by-user.md) | `POST /v1/chat/chat_session_by_uid` | [docs](https://app.alltius.ai/api/platform/documentation) |
| [Rate Response](actions/rate-response.md) | `PUT /v1/chat/rating` | [docs](https://app.alltius.ai/api/platform/documentation) |
| [Verify Connection](actions/verify-connection.md) | `POST /v1/chat` | [docs](https://app.alltius.ai/api/platform/documentation) |

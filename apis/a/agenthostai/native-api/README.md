# Agenthost.ai: Native API Reference

A consolidated summary of Agenthost.ai's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.agenthost.ai/
- **API base URL:** `https://api.agenthost.ai`

## Authentication

### API Key

Authenticate Agenthost API requests with an ag-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ag-api-key: <apiKey>
```

[Official authentication documentation](https://docs.agenthost.ai/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get User Message Limit](actions/get-user-message-limit.md) | `POST /api/openai/user_message_limit/` | [docs](https://docs.agenthost.ai/custom-actions) |
| [List Available Plans](actions/list-available-plans.md) | `GET /api/openai/available_plans` | [docs](https://docs.agenthost.ai/custom-actions) |
| [Log In](actions/log-in.md) | `POST /api/openai/log_in/` | [docs](https://docs.agenthost.ai/custom-actions) |

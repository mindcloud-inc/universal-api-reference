# GPTBots: Native API Reference

A consolidated summary of GPTBots's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.gptbots.ai/docs/api-reference
- **API base URL:** `{baseUrl}`

## Authentication

### API Key

Use a GPTBots API key with a region-specific base URL for your organization.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · The GPTBots API base URL for your organization’s data center, such as https://api-sg.gptbots.ai.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.gptbots.ai/docs/api-reference/overview)

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
| [Get Agent Information](actions/get-agent-information.md) | `GET /v1/bot/detail` | [docs](https://www.gptbots.ai/docs/api-reference/account-api/get-bot-information) |

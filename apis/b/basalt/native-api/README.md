# Basalt: Native API Reference

A consolidated summary of Basalt's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.getbasalt.ai/v1/api-reference/introduction
- **API base URL:** `https://api.getbasalt.ai`

## Authentication

### API Key

Connect to Basalt with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.getbasalt.ai/api-reference/authentication)

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
| [List Prompts](actions/list-prompts.md) | `GET /prompts` | [docs](https://docs.getbasalt.ai/v1/api-reference/prompts/list) |

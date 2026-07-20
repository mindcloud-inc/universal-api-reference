# Beyond Presence: Native API Reference

A consolidated summary of Beyond Presence's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.bey.dev/api-reference
- **API base URL:** `https://api.bey.dev`

## Authentication

### API Key

Connect with a Beyond Presence API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.bey.dev/get-started/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; maximum 50). Use `cursor` in the query string as the pagination cursor.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /v1/agents` | [docs](https://docs.bey.dev/api-reference/agents/create-agent) |
| [Create Call](actions/create-call.md) | `POST /v1/calls` | [docs](https://docs.bey.dev/api-reference/calls/create-call) |
| [Create External API Configuration](actions/create-external-api-configuration.md) | `POST /v1/external-apis` | [docs](https://docs.bey.dev/api-reference/external-apis/create-external-api-configuration) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /v1/agents/:id` | [docs](https://docs.bey.dev/api-reference/agents/delete-agent) |
| [Delete External API Configuration](actions/delete-external-api-configuration.md) | `DELETE /v1/external-apis/:id` | [docs](https://docs.bey.dev/api-reference/external-apis/delete-external-api-configuration) |
| [Get Agent](actions/get-agent.md) | `GET /v1/agents/:id` | [docs](https://docs.bey.dev/api-reference/agents/retrieve-agent) |
| [Get Avatar](actions/get-avatar.md) | `GET /v1/avatars/:id` | [docs](https://docs.bey.dev/api-reference/avatars/retrieve-avatar) |
| [Get Call](actions/get-call.md) | `GET /v1/calls/:id` | [docs](https://docs.bey.dev/api-reference/calls/retrieve-call) |
| [Get External API Configuration](actions/get-external-api-configuration.md) | `GET /v1/external-apis/:id` | [docs](https://docs.bey.dev/api-reference/external-apis/retrieve-external-api-configuration) |
| [List Agents](actions/list-agents.md) | `GET /v1/agents` | [docs](https://docs.bey.dev/api-reference/agents/list-agents) |
| [List Avatars](actions/list-avatars.md) | `GET /v1/avatars` | [docs](https://docs.bey.dev/api-reference/avatars/list-avatars) |
| [List Call Messages](actions/list-call-messages.md) | `GET /v1/calls/:id/messages` | [docs](https://docs.bey.dev/api-reference/calls/list-call-messages) |
| [List Calls](actions/list-calls.md) | `GET /v1/calls` | [docs](https://docs.bey.dev/api-reference/calls/list-calls) |
| [List External API Configurations](actions/list-external-api-configurations.md) | `GET /v1/external-apis` | [docs](https://docs.bey.dev/api-reference/external-apis/list-external-api-configurations) |
| [Update Agent](actions/update-agent.md) | `PATCH /v1/agents/:id` | [docs](https://docs.bey.dev/api-reference/agents/update-agent) |
| [Verify API Key](actions/verify-api-key.md) | `GET /v1/auth/verify` | [docs](https://docs.bey.dev/api-reference/authentication/verify-api-key) |

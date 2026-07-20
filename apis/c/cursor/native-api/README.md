# Cursor: Native API Reference

A consolidated summary of Cursor's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://cursor.com/docs/cloud-agent/api/endpoints
- **OpenAPI specification:** https://cursor.com/docs-static/cloud-agents-openapi.yaml
- **API base URL:** `https://api.cursor.com`

## Authentication

### API Key

Cursor Cloud Agents API key from the Cursor Dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://cursor.com/docs/cloud-agent/api/endpoints)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Followup](actions/add-followup.md) | `POST /v0/agents/{{id}}/followup` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [API Key Info](actions/api-key-info.md) | `GET /v0/me` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /v0/agents/{{id}}` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [Get Agent Artifact Download URL](actions/get-agent-artifact-download-url.md) | `GET /v0/agents/{{id}}/artifacts/download` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [Get Agent Conversation](actions/get-agent-conversation.md) | `GET /v0/agents/{{id}}/conversation` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [Get Agent Status](actions/get-agent-status.md) | `GET /v0/agents/{{id}}` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [Launch Agent](actions/launch-agent.md) | `POST /v0/agents` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [List Agent Artifacts](actions/list-agent-artifacts.md) | `GET /v0/agents/{{id}}/artifacts` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [List Agents](actions/list-agents.md) | `GET /v0/agents` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [List GitHub Repositories](actions/list-github-repositories.md) | `GET /v0/repositories` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [List Models](actions/list-models.md) | `GET /v0/models` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |
| [Stop Agent](actions/stop-agent.md) | `POST /v0/agents/{{id}}/stop` | [docs](https://cursor.com/docs/cloud-agent/api/endpoints) |

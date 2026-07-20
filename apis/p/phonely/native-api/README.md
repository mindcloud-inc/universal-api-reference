# Phonely: Native API Reference

A consolidated summary of Phonely's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.phonely.ai/api-reference/introduction
- **API base URL:** `https://app.phonely.ai`

## Authentication

### API Key

Authenticate requests with the Phonely API key in the X-Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.phonely.ai/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string. Supported operators: `eq`, `includes`.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Agent Documents](actions/add-agent-documents.md) | `POST /api/agent-documents` | [docs](https://docs.phonely.ai/api-reference/endpoint/post-agent-documents) |
| [Add Agent Websites](actions/add-agent-websites.md) | `POST /api/agent-websites` | [docs](https://docs.phonely.ai/api-reference/endpoint/post-agent-websites) |
| [Add Block List Numbers](actions/add-block-list-numbers.md) | `POST /api/agent-block-list` | [docs](https://docs.phonely.ai/api-reference/endpoint/block-list) |
| [Delete Agent Documents](actions/delete-agent-documents.md) | `DELETE /api/agent-documents` | [docs](https://docs.phonely.ai/api-reference/endpoint/delete-agent-documents) |
| [Delete Agent Websites](actions/delete-agent-websites.md) | `DELETE /api/agent-websites` | [docs](https://docs.phonely.ai/api-reference/endpoint/delete-agent-websites) |
| [Delete Block List Numbers](actions/delete-block-list-numbers.md) | `DELETE /api/agent-block-list` | [docs](https://docs.phonely.ai/api-reference/endpoint/block-list) |
| [Duplicate Agent](actions/duplicate-agent.md) | `POST /api/duplicate-agent` | [docs](https://docs.phonely.ai/api-reference/endpoint/duplicate-agent) |
| [Get Agent](actions/get-agent.md) | `POST /api/get-agent` | [docs](https://docs.phonely.ai/api-reference/endpoint/get-agent) |
| [Get Call](actions/get-call.md) | `POST /api/get-call` | [docs](https://docs.phonely.ai/api-reference/endpoint/get-call) |
| [Get Usage](actions/get-usage.md) | `GET /api/usage` | [docs](https://docs.phonely.ai/api-reference/endpoint/get-usage) |
| [List Agent Documents](actions/list-agent-documents.md) | `GET /api/agent-documents` | [docs](https://docs.phonely.ai/api-reference/endpoint/agent-documents) |
| [List Agent Websites](actions/list-agent-websites.md) | `GET /api/agent-websites` | [docs](https://docs.phonely.ai/api-reference/endpoint/agent-websites) |
| [List Agents](actions/list-agents.md) | `POST /api/get-agents` | [docs](https://docs.phonely.ai/api-reference/endpoint/get-agents) |
| [List Block List](actions/list-block-list.md) | `GET /api/agent-block-list` | [docs](https://docs.phonely.ai/api-reference/endpoint/block-list) |
| [List Calls](actions/list-calls.md) | `GET /api/calls/{{agentId}}` | [docs](https://docs.phonely.ai/api-reference/endpoint/list-calls) |
| [List Organizations](actions/list-organizations.md) | `GET /api/get-orgs` | [docs](https://docs.phonely.ai/api-reference/endpoint/get-orgs) |
| [List Voices](actions/list-voices.md) | `GET /api/list-voices` | [docs](https://docs.phonely.ai/api-reference/endpoint/list-voices) |
| [Set Post-Call Outcome](actions/set-post-call-outcome.md) | `PATCH /api/calls/{{agentId}}/{{callIdOrPhone}}` | [docs](https://docs.phonely.ai/api-reference/endpoint/set-post-call-outcome) |
| [Update Agent](actions/update-agent.md) | `POST /api/update-agent` | [docs](https://docs.phonely.ai/api-reference/endpoint/update-agent) |

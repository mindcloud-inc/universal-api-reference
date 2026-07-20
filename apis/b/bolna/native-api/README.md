# Bolna: Native API Reference

A consolidated summary of Bolna's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.bolna.ai/docs/api-reference/introduction
- **API base URL:** `https://api.bolna.ai`

## Authentication

### API Key

Authenticate with a Bolna API key generated from Dashboard -> Developers -> Create a new API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.bolna.ai/docs/api-reference/introduction)

## API conventions

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 20; accepted range 1–50). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /v2/agent` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/create) |
| [Create Knowledgebase from URL](actions/create-knowledgebase-from-url.md) | `POST /knowledgebase` | [docs](https://www.bolna.ai/docs/api-reference/knowledgebase/create) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /v2/agent/:agentId` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/delete) |
| [Delete Knowledgebase](actions/delete-knowledgebase.md) | `DELETE /knowledgebase/:ragId` | [docs](https://www.bolna.ai/docs/api-reference/knowledgebase/delete) |
| [Get Agent](actions/get-agent.md) | `GET /v2/agent/:agentId` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/get) |
| [Get Knowledgebase](actions/get-knowledgebase.md) | `GET /knowledgebase/:ragId` | [docs](https://www.bolna.ai/docs/api-reference/knowledgebase/get_knowledgebase) |
| [Get User Details](actions/get-user-details.md) | `GET /user/me` | [docs](https://www.bolna.ai/docs/api-reference/user/info) |
| [List Agent Batches](actions/list-agent-batches.md) | `GET /batches/:agentId/all` | [docs](https://www.bolna.ai/docs/api-reference/batches/get_batches) |
| [List Agents](actions/list-agents.md) | `GET /v2/agent/all` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/get_all) |
| [List All Agent Executions](actions/list-all-agent-executions.md) | `GET /v2/agent/:agentId/executions` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/get_all_agent_executions) |
| [List All Knowledgebases](actions/list-all-knowledgebases.md) | `GET /knowledgebase/all` | [docs](https://www.bolna.ai/docs/api-reference/knowledgebase/get_knowledgebases) |
| [List All Voices](actions/list-all-voices.md) | `GET /me/voices` | [docs](https://www.bolna.ai/docs/api-reference/voice/get_all) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /phone-numbers/all` | [docs](https://www.bolna.ai/docs/api-reference/phone-numbers/get_all) |
| [List Providers](actions/list-providers.md) | `GET /providers` | [docs](https://www.bolna.ai/docs/api-reference/providers/get) |
| [List SIP Trunks](actions/list-sip-trunks.md) | `GET /sip-trunks/trunks` | [docs](https://www.bolna.ai/docs/api-reference/sip-trunks/get_all) |
| [List Violations](actions/list-violations.md) | `GET /violations/list` | [docs](https://www.bolna.ai/docs/api-reference/violations/list) |
| [Patch Update Agent](actions/patch-update-agent.md) | `PATCH /v2/agent/:agentId` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/patch_update) |
| [Search Phone Numbers](actions/search-phone-numbers.md) | `GET /phone-numbers/search` | [docs](https://www.bolna.ai/docs/api-reference/phone-numbers/search) |
| [Stop Agent Calls](actions/stop-agent-calls.md) | `POST /v2/agent/:agentId/stop` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/stop) |
| [Update Agent](actions/update-agent.md) | `PUT /v2/agent/:agentId` | [docs](https://www.bolna.ai/docs/api-reference/agent/v2/update) |

# Release0: Native API Reference

A consolidated summary of Release0's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.release0.com
- **OpenAPI specification:** https://docs.release0.com/openapi/builder.json
- **API base URL:** `https://release0.com/api`

## Authentication

### API Key

Authenticate Release0 requests with a provider-generated API key sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.release0.com/account/apikey)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Workspace Slug](actions/check-workspace-slug.md) | `GET /v1/workspaces/:slug/exists` | [docs](https://docs.release0.com/workspace/general) |
| [Create Agent](actions/create-agent.md) | `POST /v1/agents` | [docs](https://docs.release0.com/api-reference/agent/create) |
| [Create Domain](actions/create-domain.md) | `POST /v1/domains` | [docs](https://docs.release0.com/workspace/customDomains) |
| [Create Tag](actions/create-tag.md) | `POST /v1/tags` | [docs](https://docs.release0.com/workspace/tags) |
| [Create Workspace](actions/create-workspace.md) | `POST /v1/workspaces` | [docs](https://docs.release0.com/api-reference/workspace/create) |
| [Get Agent](actions/get-agent.md) | `GET /v1/agents/:agentId` | [docs](https://docs.release0.com/api-reference/agent/get) |
| [Get Agent Analytics Stats](actions/get-agent-analytics-stats.md) | `GET /v1/agents/:agentId/analytics/stats` | [docs](https://docs.release0.com/submission/analytics) |
| [Get Published Agent](actions/get-published-agent.md) | `GET /v1/agents/:agentId/publishedAgent` | [docs](https://docs.release0.com/editor/agent-settings/publish) |
| [Get Tag](actions/get-tag.md) | `GET /v1/tags/:id` | [docs](https://docs.release0.com/workspace/tags) |
| [Get Workspace](actions/get-workspace.md) | `GET /v1/workspaces/:workspaceId` | [docs](https://docs.release0.com/api-reference/workspace/get) |
| [Import Agent](actions/import-agent.md) | `POST /v1/agents/import` | [docs](https://docs.release0.com/api-reference/agent/import) |
| [List Agent Collaborators](actions/list-agent-collaborators.md) | `GET /v1/agents/:agentId/collaborators` | [docs](https://docs.release0.com/workspace/add-members-and-guests) |
| [List Agent Result Logs](actions/list-agent-result-logs.md) | `GET /v1/agents/:agentId/results/:resultId/logs` | [docs](https://docs.release0.com/submission/realtime) |
| [List Agent Results](actions/list-agent-results.md) | `GET /v1/agents/:agentId/results` | [docs](https://docs.release0.com/submission/overview) |
| [List Agents](actions/list-agents.md) | `GET /v1/agents` | [docs](https://docs.release0.com/api-reference/agent/list) |
| [List Domains](actions/list-domains.md) | `GET /v1/domains` | [docs](https://docs.release0.com/workspace/customDomains) |
| [List Linked Agents](actions/list-linked-agents.md) | `GET /v1/agents/:agentId/linkedAgents` | [docs](https://docs.release0.com/editor/elements/logic/link-to-agent) |
| [List Tags](actions/list-tags.md) | `GET /v1/tags` | [docs](https://docs.release0.com/workspace/tags) |
| [List Workspace Members](actions/list-workspace-members.md) | `GET /v1/workspaces/:workspaceId/members` | [docs](https://docs.release0.com/api-reference/workspace/list-members) |
| [List Workspaces](actions/list-workspaces.md) | `GET /v1/workspaces` | [docs](https://docs.release0.com/api-reference/workspace/list) |
| [Publish Agent](actions/publish-agent.md) | `POST /v1/agents/:agentId/publish` | [docs](https://docs.release0.com/api-reference/agent/publish) |
| [Unpublish Agent](actions/unpublish-agent.md) | `POST /v1/agents/:agentId/unpublish` | [docs](https://docs.release0.com/api-reference/agent/unpublish) |
| [Update Agent](actions/update-agent.md) | `PATCH /v1/agents/:agentId` | [docs](https://docs.release0.com/api-reference/agent/update) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /v1/workspaces/:workspaceId` | [docs](https://docs.release0.com/api-reference/workspace/update) |
| [Verify Domain](actions/verify-domain.md) | `GET /v1/domains/:name/verify` | [docs](https://docs.release0.com/workspace/customDomains) |

# Letta: Native API Reference

A consolidated summary of Letta's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.letta.com/api
- **API base URL:** `https://api.letta.com`

## Authentication

### API Key

Letta API key authentication using an Authorization bearer token.

### Credentials

- **Letta API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.letta.com/api-overview/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `after` in the query string as the pagination cursor; numbering starts at 0.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach Tool To Agent](actions/attach-tool-to-agent.md) | `PATCH /v1/agents/:agent_id/tools/attach/:tool_id` | [docs](https://docs.letta.com/api/resources/agents/subresources/tools/methods/attach) |
| [Cancel Agent Message](actions/cancel-agent-message.md) | `POST /v1/agents/:agent_id/messages/cancel` | [docs](https://docs.letta.com/api/resources/agents/subresources/messages/methods/cancel) |
| [Create Agent](actions/create-agent.md) | `POST /v1/agents/` | [docs](https://docs.letta.com/api/resources/agents/methods/create) |
| [Create Agent Message](actions/create-agent-message.md) | `POST /v1/agents/:agent_id/messages` | [docs](https://docs.letta.com/api/resources/agents/subresources/messages/methods/create) |
| [Create Agent Message Async](actions/create-agent-message-async.md) | `POST /v1/agents/:agent_id/messages/async` | [docs](https://docs.letta.com/api/resources/agents/subresources/messages/methods/create-async) |
| [Create Block](actions/create-block.md) | `POST /v1/blocks/` | [docs](https://docs.letta.com/api/resources/blocks/methods/create) |
| [Create Tool](actions/create-tool.md) | `POST /v1/tools/` | [docs](https://docs.letta.com/api/resources/tools/methods/create) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /v1/agents/:agent_id` | [docs](https://docs.letta.com/api/resources/agents/methods/delete) |
| [Detach Tool From Agent](actions/detach-tool-from-agent.md) | `PATCH /v1/agents/:agent_id/tools/detach/:tool_id` | [docs](https://docs.letta.com/api/resources/agents/subresources/tools/methods/detach) |
| [List Agent Memory Blocks](actions/list-agent-memory-blocks.md) | `GET /v1/agents/:agent_id/core-memory/blocks` | [docs](https://docs.letta.com/api/resources/agents/subresources/blocks/methods/list) |
| [List Agent Messages](actions/list-agent-messages.md) | `GET /v1/agents/:agent_id/messages` | [docs](https://docs.letta.com/api/resources/agents/subresources/messages/methods/list) |
| [List Agent Tools](actions/list-agent-tools.md) | `GET /v1/agents/:agent_id/tools` | [docs](https://docs.letta.com/api/resources/agents/subresources/tools/methods/list) |
| [List Agents](actions/list-agents.md) | `GET /v1/agents/` | [docs](https://docs.letta.com/api/resources/agents/methods/list) |
| [List Blocks](actions/list-blocks.md) | `GET /v1/blocks/` | [docs](https://docs.letta.com/api/resources/blocks/methods/list) |
| [List Conversations](actions/list-conversations.md) | `GET /v1/conversations/` | [docs](https://docs.letta.com/api/resources/conversations/methods/list) |
| [List Models](actions/list-models.md) | `GET /v1/models/` | [docs](https://docs.letta.com/api/resources/models/methods/list) |
| [List Runs](actions/list-runs.md) | `GET /v1/runs/` | [docs](https://docs.letta.com/api/resources/runs/methods/list) |
| [List Tools](actions/list-tools.md) | `GET /v1/tools/` | [docs](https://docs.letta.com/api/resources/tools/methods/list) |
| [Reset Agent Messages](actions/reset-agent-messages.md) | `PATCH /v1/agents/:agent_id/reset-messages` | [docs](https://docs.letta.com/api/resources/agents/subresources/messages/methods/reset) |
| [Retrieve Agent](actions/retrieve-agent.md) | `GET /v1/agents/:agent_id` | [docs](https://docs.letta.com/api/resources/agents/methods/retrieve) |
| [Retrieve Agent Memory Block](actions/retrieve-agent-memory-block.md) | `GET /v1/agents/:agent_id/core-memory/blocks/:block_label` | [docs](https://docs.letta.com/api/resources/agents/subresources/blocks/methods/retrieve) |
| [Retrieve Run](actions/retrieve-run.md) | `GET /v1/runs/:run_id` | [docs](https://docs.letta.com/api/resources/runs/methods/retrieve) |
| [Summarize Agent Messages](actions/summarize-agent-messages.md) | `POST /v1/agents/:agent_id/summarize` | [docs](https://docs.letta.com/api/resources/agents/subresources/messages/methods/compact) |
| [Update Agent](actions/update-agent.md) | `PATCH /v1/agents/:agent_id` | [docs](https://docs.letta.com/api/resources/agents/methods/update) |
| [Update Agent Memory Block](actions/update-agent-memory-block.md) | `PATCH /v1/agents/:agent_id/core-memory/blocks/:block_label` | [docs](https://docs.letta.com/api/resources/agents/subresources/blocks/methods/update) |

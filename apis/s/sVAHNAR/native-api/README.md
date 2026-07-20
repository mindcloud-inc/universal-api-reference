# SVAHNAR: Native API Reference

A consolidated summary of SVAHNAR's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.svahnar.com/docs/GetStarted/Overview/
- **API base URL:** `https://api.svahnar.com`

## Authentication

### API Key

Connect with a SVAHNAR API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.svahnar.com/docs/GetStarted/Quickstart/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `agents`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Agent](actions/delete-agent.md) | `DELETE /v1/agents/delete` | [docs](https://docs.svahnar.com/docs/Agents/delete_agent/) |
| [Delete Multiple Agents](actions/delete-multiple-agents.md) | `DELETE /v1/agents/bulk-delete` | [docs](https://docs.svahnar.com/docs/Agents/delete_agent/#delete-multiple-agents) |
| [Get Agent Configuration](actions/get-agent-configuration.md) | `GET /v1/agents/download-agent/:agent_id` | [docs](https://docs.svahnar.com/docs/Agents/get_agent_details/) |
| [Get Agent Details](actions/get-agent-details.md) | `GET /v1/agents/get-agent/:agent_id` | [docs](https://docs.svahnar.com/docs/Agents/get_agent_details/) |
| [Get Credits](actions/get-credits.md) | `GET /v1/credits/get` | [docs](https://docs.svahnar.com/docs/GetStarted/Quickstart/) |
| [List All Agents](actions/list-all-agents.md) | `GET /v1/agents/list-agents` | [docs](https://docs.svahnar.com/docs/Agents/list_agents/) |
| [Login](actions/login.md) | `POST /v1/auth/login` | [docs](https://docs.svahnar.com/docs/GetStarted/Quickstart/) |
| [Run Agent](actions/run-agent.md) | `POST /v1/agents/run` | [docs](https://docs.svahnar.com/docs/Agents/run_agent/) |
| [Test Agent](actions/test-agent.md) | `POST /v1/agents/test` | [docs](https://docs.svahnar.com/docs/Agents/test_agent/) |
| [Validate Agent Configuration](actions/validate-agent-configuration.md) | `POST /v1/agents/validate` | [docs](https://docs.svahnar.com/docs/Agents/validate_config/) |

# Zaia: Native API Reference

A consolidated summary of Zaia's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.zaia.app
- **OpenAPI specification:** https://api.endless.zaia.app/openapi
- **API base URL:** `https://api.endless.zaia.app`

## Authentication

### API Key

Use a Zaia Endless workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.zaia.app/documentation/api-reference-alpha/reference/agents)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; accepted range 1–100). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | `POST /api/v1/tags` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/v1/tags/:id` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags) |
| [Get Tag](actions/get-tag.md) | `GET /api/v1/tags/:id` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags) |
| [List Agents](actions/list-agents.md) | `GET /api/v1/agents` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/agents) |
| [List Channels](actions/list-channels.md) | `GET /api/v1/channels` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/channels) |
| [List Components](actions/list-components.md) | `GET /api/v1/components` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/components) |
| [List Connections](actions/list-connections.md) | `GET /api/v1/connections` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/connections) |
| [List Datagrids](actions/list-datagrids.md) | `GET /api/v1/datagrids` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/datagrids) |
| [List Datasets](actions/list-datasets.md) | `GET /api/v1/datasets` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/datasets) |
| [List Executions](actions/list-executions.md) | `GET /api/v1/executions` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/executions) |
| [List External Users](actions/list-external-users.md) | `GET /api/v1/external-users` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/external-users) |
| [List LLM Provider Options](actions/list-llm-provider-options.md) | `GET /api/v1/llm-providers/options` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/llm-providers) |
| [List LLM Providers](actions/list-llm-providers.md) | `GET /api/v1/llm-providers` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/llm-providers) |
| [List MCP Options](actions/list-mcp-options.md) | `GET /api/v1/mcps/options` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/mcps) |
| [List MCPs](actions/list-mcps.md) | `GET /api/v1/mcps` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/mcps) |
| [List Responders](actions/list-responders.md) | `GET /api/v1/super-identities/responders` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/super-identities) |
| [List Squads](actions/list-squads.md) | `GET /api/v1/squads` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/squads) |
| [List Tags](actions/list-tags.md) | `GET /api/v1/tags` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags) |
| [List Ticketing Teams](actions/list-ticketing-teams.md) | `GET /api/v1/ticketing-teams` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/ticketing-teams) |
| [Update Tag](actions/update-tag.md) | `PATCH /api/v1/tags/:id` | [docs](https://docs.zaia.app/documentation/api-reference-alpha/reference/tags) |

# Dust: Native API Reference

A consolidated summary of Dust's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.dust.tt/reference
- **API base URL:** `https://dust.tt`

## Authentication

### API Key

Connect to Dust with a workspace API key and workspace ID.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspaceId` · required · Dust workspace ID from the workspace URL after /w/.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dust.tt/docs/make-dust-integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | `POST /api/v1/w/:workspaceId/assistant/conversations` | [docs](https://docs.dust.tt/reference/post_api-v1-w-wid-assistant-conversations) |
| [Get Conversation](actions/get-conversation.md) | `GET /api/v1/w/:workspaceId/assistant/conversations/:conversationId` | [docs](https://docs.dust.tt/reference/get_api-v1-w-wid-assistant-conversations-cid) |
| [Get Data Sources](actions/get-data-sources.md) | `GET /api/v1/w/:workspaceId/spaces/:spaceId/data_sources` | [docs](https://docs.dust.tt/reference/get_api-v1-w-wid-spaces-spaceid-data-sources) |
| [List Agents](actions/list-agents.md) | `GET /api/v1/w/:workspaceId/assistant/agent_configurations` | [docs](https://docs.dust.tt/reference/get_api-v1-w-wid-assistant-agent-configurations) |
| [List Spaces](actions/list-spaces.md) | `GET /api/v1/w/:workspaceId/spaces` | [docs](https://docs.dust.tt/reference/get_api-v1-w-wid-spaces) |
| [Search Data Source](actions/search-data-source.md) | `POST /api/v1/w/:workspaceId/spaces/:spaceId/data_sources/:dataSourceId/search` |  |
| [Upsert Document](actions/upsert-document.md) | `POST /api/v1/w/:workspaceId/spaces/:spaceId/data_sources/:dataSourceId/documents` |  |

# CustomGPT.ai: Native API Reference

A consolidated summary of CustomGPT.ai's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.customgpt.ai/reference/customgptai-api
- **OpenAPI specification:** https://docs.customgpt.ai/openapi/openapi.json
- **API base URL:** `https://app.customgpt.ai/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.customgpt.ai/docs/api-key-permissions)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `data.last_page`. The current page number is read from `data.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Source](actions/add-source.md) | `POST /projects/:projectId/sources` | [docs](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-sources-1) |
| [Create Agent](actions/create-agent.md) | `POST /projects` | [docs](https://docs.customgpt.ai/reference/post_api-v1-projects) |
| [Create Conversation](actions/create-conversation.md) | `POST /projects/:projectId/conversations` | [docs](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-conversations-1) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /projects/:projectId` | [docs](https://docs.customgpt.ai/reference/delete_api-v1-projects-projectid-1) |
| [Delete Document](actions/delete-document.md) | `DELETE /projects/:projectId/pages/:pageId` | [docs](https://docs.customgpt.ai/reference/delete_api-v1-projects-projectid-pages-pageid-1) |
| [Get Agent Details](actions/get-agent-details.md) | `GET /projects/:projectId` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid) |
| [Get Agent Settings](actions/get-agent-settings.md) | `GET /projects/:projectId/settings` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-settings-1) |
| [Get Agent Statistics](actions/get-agent-statistics.md) | `GET /projects/:projectId/stats` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-stats) |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /user` | [docs](https://docs.customgpt.ai/reference/get_api-v1-user) |
| [Get Document Metadata](actions/get-document-metadata.md) | `GET /projects/:projectId/pages/:pageId/metadata` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-pages-pageid-metadata-1) |
| [List Agents](actions/list-agents.md) | `GET /projects` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-1) |
| [List Conversations](actions/list-conversations.md) | `GET /projects/:projectId/conversations` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-conversations) |
| [List Documents](actions/list-documents.md) | `GET /projects/:projectId/pages` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-pages-1) |
| [List Sources](actions/list-sources.md) | `GET /projects/:projectId/sources` | [docs](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-sources-1) |
| [Reindex Document](actions/reindex-document.md) | `POST /projects/:projectId/pages/:pageId/reindex` | [docs](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-pages-pageid-reindex-1) |
| [Update Agent](actions/update-agent.md) | `POST /projects/:projectId` | [docs](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-1) |
| [Update Agent Settings](actions/update-agent-settings.md) | `POST /projects/:projectId/settings` | [docs](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-settings-1) |
| [Update Document Metadata](actions/update-document-metadata.md) | `PUT /projects/:projectId/pages/:pageId/metadata` | [docs](https://docs.customgpt.ai/reference/put_api-v1-projects-projectid-pages-pageid-metadata-1) |

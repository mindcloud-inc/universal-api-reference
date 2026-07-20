# Teamhood: Native API Reference

A consolidated summary of Teamhood's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://api-mindcloud1.teamhood.com/swagger/index.html
- **OpenAPI specification:** https://api-mindcloud1.teamhood.com/swagger/v1/swagger.json
- **API base URL:** `https://api-mindcloud1.teamhood.com/api/v1`

## Authentication

### API Key

Authenticate Teamhood requests with an API key sent in the X-ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-mindcloud1.teamhood.com/swagger/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `Take` in the query string to set the page size (default 100; maximum 1000). Use `Skip` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Delete Attachment](actions/delete-attachment.md) | `DELETE /attachments/:id` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Delete Item](actions/delete-item.md) | `DELETE /items/:itemId` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Download Attachment Content](actions/download-attachment-content.md) | `GET /attachments/:id/content` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Get Attachment](actions/get-attachment.md) | `GET /attachments/:id` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Get Item](actions/get-item.md) | `GET /items/:itemId` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Board Rows](actions/list-board-rows.md) | `GET /boards/:boardId/rows` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Board Statuses](actions/list-board-statuses.md) | `GET /boards/:boardId/statuses` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Board Templates](actions/list-board-templates.md) | `GET /templates/board` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Item Activities](actions/list-item-activities.md) | `POST /boards/:boardId/item-activities` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Item Attachments](actions/list-item-attachments.md) | `GET /items/:itemId/attachments` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Timelogs](actions/list-timelogs.md) | `POST /timelogs` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Workspace Boards](actions/list-workspace-boards.md) | `GET /workspaces/:workspaceId/boards` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Workspace Templates](actions/list-workspace-templates.md) | `GET /templates/workspace` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Query Items](actions/query-items.md) | `GET /items` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |
| [Update Item](actions/update-item.md) | `PUT /items/:itemId` | [docs](https://api-mindcloud1.teamhood.com/swagger/index.html) |

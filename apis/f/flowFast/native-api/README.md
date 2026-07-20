# FlowFast: Native API Reference

A consolidated summary of FlowFast's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://apps.flowfast.io
- **API base URL:** `https://apps.flowfast.io/api/latest/`

## Authentication

### API Key

Connect to FlowFast with a tenant API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apps.flowfast.io)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Board](actions/create-board.md) | `POST /spaces/:spaceId/boards` | [docs](https://apps.flowfast.io) |
| [Create Card](actions/create-card.md) | `POST /cards` | [docs](https://apps.flowfast.io) |
| [Create Card Comment](actions/create-card-comment.md) | `POST /cards/:cardId/comments` | [docs](https://apps.flowfast.io) |
| [Create Column](actions/create-column.md) | `POST /boards/:boardId/columns` | [docs](https://apps.flowfast.io) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://apps.flowfast.io) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://apps.flowfast.io) |
| [Delete Card](actions/delete-card.md) | `DELETE /cards/:cardId` | [docs](https://apps.flowfast.io) |
| [Delete Column](actions/delete-column.md) | `DELETE /boards/:boardId/columns/:columnId` | [docs](https://apps.flowfast.io) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:documentId` | [docs](https://apps.flowfast.io) |
| [Get Board](actions/get-board.md) | `GET /boards/:boardId` | [docs](https://apps.flowfast.io) |
| [Get Card](actions/get-card.md) | `GET /cards/:cardId` | [docs](https://apps.flowfast.io) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://apps.flowfast.io) |
| [Get Space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://apps.flowfast.io) |
| [List Board Columns](actions/list-board-columns.md) | `GET /boards/:boardId/columns` | [docs](https://apps.flowfast.io) |
| [List Board Lanes](actions/list-board-lanes.md) | `GET /boards/:boardId/lanes` | [docs](https://apps.flowfast.io) |
| [List Card Comments](actions/list-card-comments.md) | `GET /cards/:cardId/comments` | [docs](https://apps.flowfast.io) |
| [List Card Files](actions/list-card-files.md) | `GET /cards/:cardId/files` | [docs](https://apps.flowfast.io) |
| [List Card Tags](actions/list-card-tags.md) | `GET /cards/:cardId/tags` | [docs](https://apps.flowfast.io) |
| [List Cards](actions/list-cards.md) | `GET /cards` | [docs](https://apps.flowfast.io) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://apps.flowfast.io) |
| [List Space Boards](actions/list-space-boards.md) | `GET /spaces/:spaceId/boards` | [docs](https://apps.flowfast.io) |
| [List Space Cards](actions/list-space-cards.md) | `GET /spaces/:spaceId/cards` | [docs](https://apps.flowfast.io) |
| [List Spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://apps.flowfast.io) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://apps.flowfast.io) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://apps.flowfast.io) |
| [Update Card](actions/update-card.md) | `PATCH /cards/:cardId` | [docs](https://apps.flowfast.io) |
| [Update Card Comment](actions/update-card-comment.md) | `PATCH /cards/:cardId/comments/:commentId` | [docs](https://apps.flowfast.io) |
| [Update Column](actions/update-column.md) | `PATCH /boards/:boardId/columns/:columnId` | [docs](https://apps.flowfast.io) |
| [Update Document](actions/update-document.md) | `PATCH /documents/:documentId` | [docs](https://apps.flowfast.io) |
| [Update Lane](actions/update-lane.md) | `PATCH /boards/:boardId/lanes/:laneId` | [docs](https://apps.flowfast.io) |

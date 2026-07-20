# OneDeck: Native API Reference

A consolidated summary of OneDeck's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.onedeck.com/api
- **API base URL:** `https://{accountName}.onedeck.com/api/v1`

## Authentication

### API Key

Authenticate with a OneDeck API key sent in the auth-token header.

### Credentials

- **API Key:** `apiKey` · required
- **Account Name:** `accountName` · required · Your OneDeck account name from https://<accountName>.onedeck.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.onedeck.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | `POST /boards/{{boardId}}/records` | [docs](https://www.onedeck.com/api) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://www.onedeck.com/api) |
| [Get Record](actions/get-record.md) | `GET /boards/{{boardId}}/records/{{recordId}}` | [docs](https://www.onedeck.com/api) |
| [Invite Share Studio User](actions/invite-share-studio-user.md) | `POST /share-studio/:shareId/invite` | [docs](https://www.onedeck.com/api) |
| [List Board Fields](actions/list-board-fields.md) | `GET /boards/{{boardId}}/fields` | [docs](https://www.onedeck.com/api) |
| [List Boards](actions/list-boards.md) | `GET /boards` | [docs](https://www.onedeck.com/api) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://www.onedeck.com/api) |
| [List Records](actions/list-records.md) | `GET /boards/{{boardId}}/records` | [docs](https://www.onedeck.com/api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.onedeck.com/api) |
| [Update Record](actions/update-record.md) | `PUT /boards/{{boardId}}/records/{{recordId}}` | [docs](https://www.onedeck.com/api) |
| [Upload Record Attachment](actions/upload-record-attachment.md) | `POST /boards/{{boardId}}/records/{{recordId}}/attachments` | [docs](https://www.onedeck.com/api) |

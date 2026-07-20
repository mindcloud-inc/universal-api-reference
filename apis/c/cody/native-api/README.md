# Cody: Native API Reference

A consolidated summary of Cody's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.meetcody.ai/
- **OpenAPI specification:** https://developers.meetcody.ai/source.json
- **API base URL:** `https://getcody.ai/api/v1`

## Authentication

### API Key

Use a Cody API key with an Authorization header in the format Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.meetcody.ai/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://developers.meetcody.ai/operation/operation-create-conversation) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://developers.meetcody.ai/operation/operation-create-document) |
| [Create Document from File](actions/create-document-from-file.md) | `POST /documents/file` | [docs](https://developers.meetcody.ai/operation/operation-create-document-from-file) |
| [Create Document from Webpage](actions/create-document-from-webpage.md) | `POST /documents/webpage` | [docs](https://developers.meetcody.ai/operation/operation-create-document-from-webpage) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://developers.meetcody.ai/operation/operation-create-folder) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /conversations/:id` | [docs](https://developers.meetcody.ai/operation/operation-delete-conversation) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:id` | [docs](https://developers.meetcody.ai/operation/operation-delete-document) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:id` | [docs](https://developers.meetcody.ai/operation/operation-get-conversation) |
| [Get Document](actions/get-document.md) | `GET /documents/:id` | [docs](https://developers.meetcody.ai/operation/operation-get-document) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:id` | [docs](https://developers.meetcody.ai/operation/operation-get-folder) |
| [Get Message](actions/get-message.md) | `GET /messages/:id` | [docs](https://developers.meetcody.ai/operation/operation-get-message) |
| [Get Upload URL](actions/get-upload-url.md) | `POST /uploads/signed-url` | [docs](https://developers.meetcody.ai/operation/operation-get-uploads-signed-url) |
| [List Bots](actions/list-bots.md) | `GET /bots` | [docs](https://developers.meetcody.ai/operation/operation-list-bots) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developers.meetcody.ai/operation/operation-list-conversations) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://developers.meetcody.ai/operation/operation-list-documents) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://developers.meetcody.ai/operation/operation-list-folders) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://developers.meetcody.ai/operation/operation-list-messages) |
| [Send Message](actions/send-message.md) | `POST /messages` | [docs](https://developers.meetcody.ai/operation/operation-send-message) |
| [Send Message for Stream](actions/send-message-for-stream.md) | `POST /messages/stream` | [docs](https://developers.meetcody.ai/operation/operation-send-message-for-stream) |
| [Update Conversation](actions/update-conversation.md) | `POST /conversations/:id` | [docs](https://developers.meetcody.ai/operation/operation-update-conversation) |
| [Update Folder](actions/update-folder.md) | `POST /folders/:id` | [docs](https://developers.meetcody.ai/operation/operation-update-folder) |

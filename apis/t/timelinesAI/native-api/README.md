# TimelinesAI: Native API Reference

A consolidated summary of TimelinesAI's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://timelinesai.mintlify.app/public-api-reference/overview
- **OpenAPI specification:** https://timelinesai.mintlify.app/openapi/public_api_spec.yaml
- **API base URL:** `https://app.timelines.ai/integrations/api`

## Authentication

### Public API Token

Use a TimelinesAI Public API bearer token from the Public API settings page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://timelinesai.mintlify.app/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Chat Labels](actions/add-chat-labels.md) | `PUT /chats/{chat_id}/labels` | [docs](https://timelinesai.mintlify.app/public-api-reference/adds-labels-for-the-chat) |
| [Add Chat Note](actions/add-chat-note.md) | `POST /chats/{chat_id}/notes` | [docs](https://timelinesai.mintlify.app/public-api-reference/add-a-note-to-existing-chat) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://timelinesai.mintlify.app/public-api-reference/create-webhook) |
| [Get Chat](actions/get-chat.md) | `GET /chats/{chat_id}` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-details-of-a-chat) |
| [Get File](actions/get-file.md) | `GET /files/{file_uid}` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-details-and-temporary-download-url-for-a-specified-uploaded-file) |
| [Get Message](actions/get-message.md) | `GET /messages/{message_uid}` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-the-details-of-a-message-specified-by-the-messages-uid) |
| [Get Message Reactions](actions/get-message-reactions.md) | `GET /messages/{message_uid}/reactions` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-the-current-reactions-map-for-a-message) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhook_id}` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-webhook) |
| [Get Workspace Quotas](actions/get-workspace-quotas.md) | `GET /quotas` | [docs](https://timelinesai.mintlify.app/public-api-reference/all-current-quotas-and-utilization-stats) |
| [List Chat Labels](actions/list-chat-labels.md) | `GET /chats/{chat_id}/labels` | [docs](https://timelinesai.mintlify.app/public-api-reference/list-labels-for-the-specified-chat) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /chats/{chat_id}/messages` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-filtered-chat-history-messages-only-of-the-chat) |
| [List Chats](actions/list-chats.md) | `GET /chats` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-full-or-filtered-list-of-all-chats-in-the-workspace) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://timelinesai.mintlify.app/public-api-reference/list-files-uploaded-in-your-timelinesai-workspace) |
| [List Message Status History](actions/list-message-status-history.md) | `GET /messages/{message_uid}/status_history` | [docs](https://timelinesai.mintlify.app/public-api-reference/get-the-sending-history-of-a-message-specified-by-the-messages-uid) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://timelinesai.mintlify.app/public-api-reference/list-webhooks) |
| [List WhatsApp Accounts](actions/list-whatsapp-accounts.md) | `GET /whatsapp_accounts` | [docs](https://timelinesai.mintlify.app/public-api-reference/list-whatsapp-accounts-connected-in-your-timelinesai-workspace) |
| [List Workspace Teammates](actions/list-workspace-teammates.md) | `GET /teammates` | [docs](https://timelinesai.mintlify.app/public-api-reference/list-all-teammates-in-the-workspace) |
| [Replace Chat Labels](actions/replace-chat-labels.md) | `POST /chats/{chat_id}/labels` | [docs](https://timelinesai.mintlify.app/public-api-reference/replaces-labels-for-the-chat) |
| [Send Chat Message](actions/send-chat-message.md) | `POST /chats/{chat_id}/messages` | [docs](https://timelinesai.mintlify.app/public-api-reference/send-message-in-existing-chat) |
| [Send Message To Chat Name](actions/send-message-to-chat-name.md) | `POST /messages/to_chat_name` | [docs](https://timelinesai.mintlify.app/public-api-reference/send-message-in-existing-chat-specified-by-chat-name) |
| [Send Message to JID](actions/send-message-to-jid.md) | `POST /messages/to_jid` | [docs](https://timelinesai.mintlify.app/public-api-reference/send-message-to-jid) |
| [Send Message to Phone](actions/send-message-to-phone.md) | `POST /messages` | [docs](https://timelinesai.mintlify.app/public-api-reference/send-message-to-phone-number) |
| [Send Voice Message To Chat](actions/send-voice-message-to-chat.md) | `POST /chats/{chat_id}/voice_message` | [docs](https://timelinesai.mintlify.app/public-api-reference/post-chats-voice_message) |
| [Update Chat](actions/update-chat.md) | `PATCH /chats/{chat_id}` | [docs](https://timelinesai.mintlify.app/public-api-reference/update-chat) |
| [Update Message Reactions](actions/update-message-reactions.md) | `PATCH /messages/{message_uid}/reactions` | [docs](https://timelinesai.mintlify.app/public-api-reference/update-reactions-for-a-message) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/{webhook_id}` | [docs](https://timelinesai.mintlify.app/public-api-reference/update-webhook) |
| [Upload File by Form](actions/upload-file-by-form.md) | `POST /files_upload` | [docs](https://timelinesai.mintlify.app/public-api-reference/upload-a-file-in-x-form-encoded-http-request) |
| [Upload File by URL](actions/upload-file-by-url.md) | `POST /files` | [docs](https://timelinesai.mintlify.app/public-api-reference/upload-a-file-using-a-publicly-accessible-url) |

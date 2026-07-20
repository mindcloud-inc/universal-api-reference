# Agent Mail: Native API Reference

A consolidated summary of Agent Mail's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.agentmail.to/api-reference
- **OpenAPI specification:** https://docs.agentmail.to/openapi.json
- **API base URL:** `https://api.agentmail.to/v0`

## Authentication

### API Key

Authenticate with an AgentMail API key using bearer token auth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.agentmail.to/api-reference/inboxes/list)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `next_page_token`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page_token` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Inbox](actions/create-inbox.md) | `POST /inboxes` | [docs](https://docs.agentmail.to/api-reference/inboxes/create) |
| [Create Inbox Draft](actions/create-inbox-draft.md) | `POST /inboxes/{inbox_id}/drafts` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/create) |
| [Create Inbox List Entry](actions/create-inbox-list-entry.md) | `POST /inboxes/{inbox_id}/lists/{direction}/{type}` | [docs](https://docs.agentmail.to/api-reference/inboxes/lists/create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.agentmail.to/api-reference/webhooks/create) |
| [Delete Inbox](actions/delete-inbox.md) | `DELETE /inboxes/{inbox_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/delete) |
| [Delete Inbox Draft](actions/delete-inbox-draft.md) | `DELETE /inboxes/{inbox_id}/drafts/{draft_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/delete) |
| [Delete Inbox List Entry](actions/delete-inbox-list-entry.md) | `DELETE /inboxes/{inbox_id}/lists/{direction}/{type}/{entry}` | [docs](https://docs.agentmail.to/api-reference/inboxes/lists/delete) |
| [Delete Inbox Message](actions/delete-inbox-message.md) | `DELETE /inboxes/{inbox_id}/messages/{message_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/delete) |
| [Delete Inbox Thread](actions/delete-inbox-thread.md) | `DELETE /inboxes/{inbox_id}/threads/{thread_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/threads/delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{webhook_id}` | [docs](https://docs.agentmail.to/api-reference/webhooks/delete) |
| [Forward Inbox Message](actions/forward-inbox-message.md) | `POST /inboxes/{inbox_id}/messages/{message_id}/forward` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/forward) |
| [Get Inbox](actions/get-inbox.md) | `GET /inboxes/{inbox_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/get) |
| [Get Inbox Draft](actions/get-inbox-draft.md) | `GET /inboxes/{inbox_id}/drafts/{draft_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/get) |
| [Get Inbox Draft Attachment](actions/get-inbox-draft-attachment.md) | `GET /inboxes/{inbox_id}/drafts/{draft_id}/attachments/{attachment_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/get-attachment) |
| [Get Inbox List Entry](actions/get-inbox-list-entry.md) | `GET /inboxes/{inbox_id}/lists/{direction}/{type}/{entry}` | [docs](https://docs.agentmail.to/api-reference/inboxes/lists/get) |
| [Get Inbox Message](actions/get-inbox-message.md) | `GET /inboxes/{inbox_id}/messages/{message_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/get) |
| [Get Inbox Message Attachment](actions/get-inbox-message-attachment.md) | `GET /inboxes/{inbox_id}/messages/{message_id}/attachments/{attachment_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/get-attachment) |
| [Get Inbox Thread](actions/get-inbox-thread.md) | `GET /inboxes/{inbox_id}/threads/{thread_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/threads/get) |
| [Get Inbox Thread Attachment](actions/get-inbox-thread-attachment.md) | `GET /inboxes/{inbox_id}/threads/{thread_id}/attachments/{attachment_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/threads/get-attachment) |
| [Get Organization](actions/get-organization.md) | `GET /organizations` | [docs](https://docs.agentmail.to/api-reference/organizations/get) |
| [Get Raw Inbox Message](actions/get-raw-inbox-message.md) | `GET /inboxes/{inbox_id}/messages/{message_id}/raw` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/get-raw) |
| [Get Thread](actions/get-thread.md) | `GET /threads/{thread_id}` | [docs](https://docs.agentmail.to/api-reference/threads/get) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhook_id}` | [docs](https://docs.agentmail.to/api-reference/webhooks/get) |
| [List Drafts](actions/list-drafts.md) | `GET /drafts` | [docs](https://docs.agentmail.to/api-reference/drafts/list) |
| [List Inbox Drafts](actions/list-inbox-drafts.md) | `GET /inboxes/{inbox_id}/drafts` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/list) |
| [List Inbox List Entries](actions/list-inbox-list-entries.md) | `GET /inboxes/{inbox_id}/lists/{direction}/{type}` | [docs](https://docs.agentmail.to/api-reference/inboxes/lists/list) |
| [List Inbox Messages](actions/list-inbox-messages.md) | `GET /inboxes/{inbox_id}/messages` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/list) |
| [List Inbox Threads](actions/list-inbox-threads.md) | `GET /inboxes/{inbox_id}/threads` | [docs](https://docs.agentmail.to/api-reference/inboxes/threads/list) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inboxes` | [docs](https://docs.agentmail.to/api-reference/inboxes/list) |
| [List Threads](actions/list-threads.md) | `GET /threads` | [docs](https://docs.agentmail.to/api-reference/threads/list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.agentmail.to/api-reference/webhooks/list) |
| [Reply All To Inbox Message](actions/reply-all-to-inbox-message.md) | `POST /inboxes/{inbox_id}/messages/{message_id}/reply-all` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/reply-all) |
| [Reply To Inbox Message](actions/reply-to-inbox-message.md) | `POST /inboxes/{inbox_id}/messages/{message_id}/reply` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/reply) |
| [Send Inbox Draft](actions/send-inbox-draft.md) | `POST /inboxes/{inbox_id}/drafts/{draft_id}/send` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/send) |
| [Send Inbox Message](actions/send-inbox-message.md) | `POST /inboxes/{inbox_id}/messages/send` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/send) |
| [Update Inbox](actions/update-inbox.md) | `PATCH /inboxes/{inbox_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/update) |
| [Update Inbox Draft](actions/update-inbox-draft.md) | `PATCH /inboxes/{inbox_id}/drafts/{draft_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/drafts/update) |
| [Update Inbox Message](actions/update-inbox-message.md) | `PATCH /inboxes/{inbox_id}/messages/{message_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/messages/update) |
| [Update Inbox Thread](actions/update-inbox-thread.md) | `PATCH /inboxes/{inbox_id}/threads/{thread_id}` | [docs](https://docs.agentmail.to/api-reference/inboxes/threads/update) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/{webhook_id}` | [docs](https://docs.agentmail.to/api-reference/webhooks/update) |

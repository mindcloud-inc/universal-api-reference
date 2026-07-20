# SparrowDesk: Native API Reference

A consolidated summary of SparrowDesk's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developer.sparrowdesk.com/rest-api
- **API base URL:** `https://api.sparrowdesk.com/v1`

## Authentication

### API Key

Use a SparrowDesk API key from Settings > API keys. Requests authenticate with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.sparrowdesk.com/rest-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Conversation Reply](actions/add-conversation-reply.md) | `POST /conversations/{{id}}/reply` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/reply/post) |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | `POST /bulk/contacts` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/bulk/contacts/post) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/contacts/post) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/post) |
| [Create Conversation Field](actions/create-conversation-field.md) | `POST /conversations/fields` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/fields/post) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/contacts/id/delete) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /conversations/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/delete) |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | `GET /bulk/status/{{jobId}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/bulk/status/jobid/get) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/contacts/id/get) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/get) |
| [Get Conversation Field](actions/get-conversation-field.md) | `GET /conversations/fields/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/fields/id/get) |
| [Get Current Account](actions/get-current-account.md) | `GET /me` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/me/get) |
| [List Contact Fields](actions/list-contact-fields.md) | `GET /contact-fields` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/contact-fields/get) |
| [List Conversation Fields](actions/list-conversation-fields.md) | `GET /conversations/fields` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/fields/get) |
| [List Conversation Replies](actions/list-conversation-replies.md) | `GET /conversations/{{id}}/replies` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/replies/get) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/get) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/members/get) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/tags/get) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/contacts/id/patch) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /conversations/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/id/patch) |
| [Update Conversation Field](actions/update-conversation-field.md) | `PATCH /conversations/fields/{{id}}` | [docs](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/fields/id/patch) |

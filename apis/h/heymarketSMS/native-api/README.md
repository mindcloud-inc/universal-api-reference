# Heymarket SMS: Native API Reference

A consolidated summary of Heymarket SMS's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://heymarket.docs.apiary.io/
- **API base URL:** `https://api.heymarket.com`

## Authentication

### API Key

Authenticate with a Heymarket Team API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://heymarket.docs.apiary.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size. Use `page` in the request body to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the request body. Set the direction separately with `ascending`. Use `true` for ascending order and `false` for descending order. Only one sort field is accepted.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Create Contacts](actions/batch-create-contacts.md) | `POST /v1/batch/contacts` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Close Conversation](actions/close-conversation.md) | `POST /v1/conversations/close` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contact` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Create Schedule](actions/create-schedule.md) | `POST /v1/schedule` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Create Template](actions/create-template.md) | `POST /v1/template` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contact/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Contact Status](actions/get-contact-status.md) | `POST /v1/contact/status` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Conversation](actions/get-conversation.md) | `GET /v1/conversations/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Conversation Message History](actions/get-conversation-message-history.md) | `GET /v1/messages` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Schedule](actions/get-schedule.md) | `GET /v1/schedule/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Template](actions/get-template.md) | `GET /v1/template/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Get Users](actions/get-users.md) | `GET /v1/users/get` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [List Contact Fields](actions/list-contact-fields.md) | `POST /v1/contact-fields` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [List Contacts](actions/list-contacts.md) | `POST /v1/contacts` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [List Conversations](actions/list-conversations.md) | `POST /v1/conversations` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [List Inboxes](actions/list-inboxes.md) | `GET /v1/inboxes` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [List Team Messages](actions/list-team-messages.md) | `POST /v1/messages/all` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [List Templates](actions/list-templates.md) | `POST /v1/templates` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Mark Conversation Read](actions/mark-conversation-read.md) | `POST /v1/conversations/read` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Mark Conversation Unread](actions/mark-conversation-unread.md) | `POST /v1/conversations/unread` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Open Conversation](actions/open-conversation.md) | `POST /v1/conversations/open` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Reassign Conversation](actions/reassign-conversation.md) | `POST /v1/conversations/reassign` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Send Message](actions/send-message.md) | `POST /v1/message/send` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Set Contact Status](actions/set-contact-status.md) | `POST /v1/contact/set_status` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Update Contact](actions/update-contact.md) | `PUT /v1/contact/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Update Schedule](actions/update-schedule.md) | `PUT /v1/schedule/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
| [Update Template](actions/update-template.md) | `PUT /v1/template/:id` | [docs](https://heymarket.docs.apiary.io/api-description-document) |
